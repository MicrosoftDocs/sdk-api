---
UID: TP:serports
ms.assetid: a99541fb-a2d1-3e81-9efd-97d9eecc1ed4
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Serial Controller Driver Reference



Overview of the Serial Controller Driver Reference technology.

To develop Serial Controller Driver Reference, you need these headers:

 * [msports.h](..\msports\index.md)

For the programming guide, see [Serial Controller Driver Reference](https://review.docs.microsoft.com/en-us/win32-test/serports).

## Functions

| Title   | Description   |
| ---- |:---- |
| [ComDBClaimNextFreePort function](..\msports\nf-msports-comdbclaimnextfreeport.md) | ComDBClaimNextFreePort returns the lowest COM port number that is not already in use. |
| [ComDBClaimPort function](..\msports\nf-msports-comdbclaimport.md) | ComDBClaimPort logs an unused COM port number as &#0034;in use&#0034; in the COM port database. |
| [ComDBClose function](..\msports\nf-msports-comdbclose.md) | ComDBClose closes a handle to the COM port database. |
| [ComDBGetCurrentPortUsage function](..\msports\nf-msports-comdbgetcurrentportusage.md) | ComDBGetCurrentPortUsage returns information about the COM port numbers that are currently logged as &#0034;in use&#0034; in the COM port database. |
| [ComDBOpen function](..\msports\nf-msports-comdbopen.md) | ComDBOpen returns a handle to the COM port database. |
| [ComDBReleasePort function](..\msports\nf-msports-comdbreleaseport.md) | ComDBReleasePort releases a COM port number in the COM port database. |
| [ComDBResizeDatabase function](..\msports\nf-msports-comdbresizedatabase.md) | ComDBResizeDatabase resizes the COM port database. |
| [SerialDisplayAdvancedSettings function](..\msports\nf-msports-serialdisplayadvancedsettings.md) | SerialDisplayAdvancedSettings displays the system-supplied advanced settings dialog box for a specified COM port device. |
