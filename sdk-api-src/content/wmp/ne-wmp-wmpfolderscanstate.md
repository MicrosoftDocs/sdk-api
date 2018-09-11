---
UID: NE:wmp.WMPFolderScanState
title: WMPFolderScanState
author: windows-sdk-content
description: The WMPFolderScanState enumeration type defines the possible operational states of Windows Media Player as it monitors file folders for digital media content.
old-location: wmp\wmpfolderscanstate.htm
tech.root: WMP
ms.assetid: 20909420-5f90-4334-b21a-82d6cdc6d019
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WMPFolderScanState, WMPFolderScanState enumeration [Windows Media Player], wmp.wmpfolderscanstate, wmp/WMPFolderScanState, wmp/wmpfssScanning, wmp/wmpfssStopped, wmp/wmpfssUnknown, wmp/wmpfssUpdating, wmpfssScanning, wmpfssStopped, wmpfssUnknown, wmpfssUpdating
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPFolderScanState
product: Windows
targetos: Windows
req.typenames: WMPFolderScanState
req.redist: 
---

# WMPFolderScanState enumeration


## -description



The <b>WMPFolderScanState</b> enumeration type defines the possible operational states of Windows Media Player as it monitors file folders for digital media content.




## -enum-fields




### -field wmpfssUnknown

Not a valid state.


### -field wmpfssScanning

Scanning folders.


### -field wmpfssUpdating

Updating the library.


### -field wmpfssStopped

Folder monitoring is stopped.


## -remarks



A scanning operation consists of two phases: scanning and updating. During the first phase, Windows Media Player determines which digital media files to add to the library. During the second phase, the Player adds the files. You can determine the current scan state by calling <b>IWMPFolderMonitorServices::get_scanState</b> or by handling the <b>FolderScanStateChange</b> event.

Windows Media Player 10 Mobile: This enumeration is not supported.




## -see-also




<a href="https://msdn.microsoft.com/90689fb7-656d-4c06-a0a9-02bbe0e5b5dd">Enumeration Types</a>



<a href="https://msdn.microsoft.com/07e9a49b-19a6-4ed2-b037-fe44ada920a1">IWMPEvents3::FolderScanStateChange</a>



<a href="https://msdn.microsoft.com/4f13d2d0-5d8c-4aa7-bc69-c5c0436337a6">IWMPFolderMonitorServices::get_scanState</a>
 

 

