---
UID: TP:hidpi
ms.assetid: 5b09bc45-2b4f-30c9-962e-404065d34cad
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# High DPI



Overview of the High DPI technology.

To develop High DPI, you need these headers:

 * [shellscalingapi.h](..\shellscalingapi\index.md)

For the programming guide, see [High DPI](/windows/desktop/hidpi).

## Functions

| Title   | Description   |
| ---- |:---- |
| [GetDpiForMonitor function](..\shellscalingapi\nf-shellscalingapi-getdpiformonitor.md) | Queries the dots per inch (dpi) of a display. |
| [GetProcessDpiAwareness function](..\shellscalingapi\nf-shellscalingapi-getprocessdpiawareness.md) | Retrieves the dots per inch (dpi) awareness of the specified process. |
| [SetProcessDpiAwareness function](..\shellscalingapi\nf-shellscalingapi-setprocessdpiawareness.md) | Sets the process-default DPI awareness level. This is equivalent to calling SetProcessDpiAwarenessContext with the corresponding DPI_AWARENESS_CONTEXT value. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [MONITOR_DPI_TYPE enumeration](..\shellscalingapi\ne-shellscalingapi-monitor_dpi_type.md) | Identifies the dots per inch (dpi) setting for a monitor. |
| [PROCESS_DPI_AWARENESS enumeration](..\shellscalingapi\ne-shellscalingapi-process_dpi_awareness.md) | Identifies dots per inch (dpi) awareness values. DPI awareness indicates how much scaling work an application performs for DPI versus how much is done by the system. |
