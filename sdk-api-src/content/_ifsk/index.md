---
UID: TP:ifsk
ms.assetid: c842e40c-3483-3721-b6bf-4da6e333af1a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Installable file systems DDI reference



Overview of the Installable file systems DDI reference technology.

To develop Installable file systems DDI reference, you need these headers:

 * [fltuser.h](..\fltuser\index.md)

For the programming guide, see [Installable file systems DDI reference](/windows/desktop/ifsk).

## Functions

| Title   | Description   |
| ---- |:---- |
| [FilterAttach function](..\fltuser\nf-fltuser-filterattach.md) | The FilterAttach function attaches a new minifilter instance to the given volume. |
| [FilterAttachAtAltitude function](..\fltuser\nf-fltuser-filterattachataltitude.md) | The FilterAttachAtAltitude function is a debugging support function that attaches a new minifilter instance to a volume at a specified altitude, overriding any settings in the minifilter's setup information (INF) file. |
| [FilterClose function](..\fltuser\nf-fltuser-filterclose.md) | The FilterClose function closes an open minifilter handle. |
| [FilterConnectCommunicationPort function](..\fltuser\nf-fltuser-filterconnectcommunicationport.md) | FilterConnectCommunicationPort opens a new connection to a communication server port that is created by a file system minifilter. |
| [FilterCreate function](..\fltuser\nf-fltuser-filtercreate.md) | The FilterCreate function creates a handle for the given minifilter. |
| [FilterDetach function](..\fltuser\nf-fltuser-filterdetach.md) | The FilterDetach function detaches the given minifilter instance from the given volume. |
| [FilterFindClose function](..\fltuser\nf-fltuser-filterfindclose.md) | The FilterFindClose function closes the specified minifilter search handle. The FilterFindFirst and FilterFindNext functions use this search handle to locate minifilters. |
| [FilterFindFirst function](..\fltuser\nf-fltuser-filterfindfirst.md) | The FilterFindFirst function returns information about a filter driver (minifilter driver instance or legacy filter driver) and is used to begin scanning the filters in the global list of registered filters. |
| [FilterFindNext function](..\fltuser\nf-fltuser-filterfindnext.md) | The FilterFindNext function continues a filter search started by a call to FilterFindFirst. |
| [FilterGetDosName function](..\fltuser\nf-fltuser-filtergetdosname.md) | The FilterGetDosName function returns the MS-DOS device name that corresponds to the given volume name. |
| [FilterGetInformation function](..\fltuser\nf-fltuser-filtergetinformation.md) | The FilterGetInformation function returns various kinds of information about a minifilter. |
| [FilterGetMessage function](..\fltuser\nf-fltuser-filtergetmessage.md) | The FilterGetMessage function gets a message from a kernel-mode minifilter. |
| [FilterInstanceClose function](..\fltuser\nf-fltuser-filterinstanceclose.md) | The FilterInstanceClose function closes a minifilter instance handle opened by FilterInstanceCreate. |
| [FilterInstanceCreate function](..\fltuser\nf-fltuser-filterinstancecreate.md) | The FilterInstanceCreate function creates a handle that can be used to communicate with the given minifilter instance. |
| [FilterInstanceFindClose function](..\fltuser\nf-fltuser-filterinstancefindclose.md) | The FilterInstanceFindClose function closes the specified minifilter instance search handle. The FilterInstanceFindFirst and FilterInstanceFindNext functions use this search handle to locate instances of a minifilter. |
| [FilterInstanceFindFirst function](..\fltuser\nf-fltuser-filterinstancefindfirst.md) | The FilterInstanceFindFirst function returns information about a minifilter driver instance and is used as a starting point for scanning the instances of a minifilter. |
| [FilterInstanceFindNext function](..\fltuser\nf-fltuser-filterinstancefindnext.md) | The FilterInstanceFindNext function continues a minifilter driver instance search started by a call to FilterInstanceFindFirst. |
| [FilterInstanceGetInformation function](..\fltuser\nf-fltuser-filterinstancegetinformation.md) | The FilterInstanceGetInformation function returns various kinds of information about a minifilter instance. |
| [FilterLoad function](..\fltuser\nf-fltuser-filterload.md) | The FilterLoad function dynamically loads a minifilter driver into the system. |
| [FilterReplyMessage function](..\fltuser\nf-fltuser-filterreplymessage.md) | The FilterReplyMessage function replies to a message from a kernel-mode minifilter. |
| [FilterSendMessage function](..\fltuser\nf-fltuser-filtersendmessage.md) | The FilterSendMessage function sends a message to a kernel-mode minifilter. |
| [FilterUnload function](..\fltuser\nf-fltuser-filterunload.md) | An application that has loaded a supporting minifilter by calling FilterLoad can unload the minifilter by calling the FilterUnload function. |
| [FilterVolumeFindClose function](..\fltuser\nf-fltuser-filtervolumefindclose.md) | The FilterVolumeFindClose function closes the specified volume search handle. FilterVolumeFindFirst and FilterVolumeFindNext use this search handle to locate volumes. |
| [FilterVolumeFindFirst function](..\fltuser\nf-fltuser-filtervolumefindfirst.md) | The FilterVolumeFindFirst function returns information about a volume. |
| [FilterVolumeFindNext function](..\fltuser\nf-fltuser-filtervolumefindnext.md) | The FilterVolumeFindNext function continues a volume search started by a call to FilterVolumeFindFirst. |
| [FilterVolumeInstanceFindClose function](..\fltuser\nf-fltuser-filtervolumeinstancefindclose.md) | The FilterVolumeInstanceFindClose function closes the specified volume instance search handle. FilterVolumeInstanceFindFirst and FilterVolumeInstanceFindNext use this search handle to locate instances on a volume. |
| [FilterVolumeInstanceFindFirst function](..\fltuser\nf-fltuser-filtervolumeinstancefindfirst.md) | The FilterVolumeInstanceFindFirst function returns information about a minifilter driver instance or legacy filter driver and is used to begin scanning the filter drivers that are attached to a volume. |
| [FilterVolumeInstanceFindNext function](..\fltuser\nf-fltuser-filtervolumeinstancefindnext.md) | The FilterVolumeInstanceFindNext function continues a minifilter driver instance or legacy filter driver search started by a call to FilterVolumeInstanceFindFirst. |
