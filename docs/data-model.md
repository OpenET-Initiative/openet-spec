# Data Model

The OpenET data model defines standardized objects for representing eye-tracking data across devices, APIs, and storage formats. These schemas are designed to be compatible with existing research standards such as **Eye-tracking-BIDS**, while also supporting **real-time streaming APIs** and **device interoperability**. Please use Gdocs/itHub PRs, issues, or discussions to contribute or suggest changes.

---

## Geom

Geom layer defines reusable geometric primitives, which serve as reusable blocks for all spatial representations

### Coordinate

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/geom.coordinate.json"
    ```


### Vector

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/geom.vector.json"
    ```


### Angle

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/geom.angle.json"
    ```


---

## Metadata

The metadata layer adds essential context, describing acquisition setups (hardware, session) and data organization (columns, signals).

### Column

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/metadata.column.json"
    ```

### Hardware

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/metadata.hardware.json"
    ```

### Session

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/metadata.session.json"
    ```

### Signals

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/metadata.signals.json"
    ```

---

## Raw

The raw layer represents raw signals from eye-tracking hardware such as eyelid state, eyeball position, gaze vectors, and pupil measurements.

### Gaze

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/raw.gaze.json"
    ```
### eyeBall

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/raw.eyeBall.json"
    ```

### eyeLid

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/raw.eyeLid.json"
    ```

### Pupil

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/raw.pupil.json"
    ```

---

## Event

The event layer captures derived measures of fixations, saccades, blinks, etc., independent of device-specific detection methods.

### Blink

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/event.blink.json"
    ```

### Fixation

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/event.fixation.json"
    ```

### Saccade

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/event.saccade.json"
    ```

---

### External event marker

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/event.marker.json"
    ```

---

## Metrics

Higher-order metrics computed from raw signals and events are defined in this layer.

### Gaze Velocity

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/metrics.velocity.json"
    ```

---

### Gaze Entropy

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/metrics.entropy.json"
    ```

---


## Misc.

Misc. layer handles logistical and operational context such as authentication and network-related information.



<!-- ## FrameReference

The `FrameReference` object links eye-tracking samples to frames in a video stream. It provides a mapping between timestamps and frame identifiers, enabling synchronization between gaze data and scene or screen recordings.

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/gaze_sample.schema.json"
    ```

---

## Stream

The `Stream` object describes a data stream exposed by an eye-tracking device or processing pipeline. It includes identifiers, stream type (e.g., gaze, pupil, fixation, video), sampling rate, and encoding format. This schema enables standardized discovery and connection to real-time data streams in OpenET systems.

??? "JSON Schema"

    ```json
    --8<-- "spec/schemas/gaze_sample.schema.json"
    ``` -->
