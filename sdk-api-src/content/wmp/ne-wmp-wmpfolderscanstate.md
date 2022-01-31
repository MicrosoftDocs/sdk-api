---
UID: NE:wmp.WMPFolderScanState
title: WMPFolderScanState (wmp.h)
description: The WMPFolderScanState enumeration type defines the possible operational states of Windows Media Player as it monitors file folders for digital media content.
helpviewer_keywords: ["WMPFolderScanState","WMPFolderScanState enumeration [Windows Media Player]","wmp.wmpfolderscanstate","wmp/WMPFolderScanState","wmp/wmpfssScanning","wmp/wmpfssStopped","wmp/wmpfssUnknown","wmp/wmpfssUpdating","wmpfssScanning","wmpfssStopped","wmpfssUnknown","wmpfssUpdating"]
old-location: wmp\wmpfolderscanstate.htm
tech.root: WMP
ms.assetid: 20909420-5f90-4334-b21a-82d6cdc6d019
ms.date: 12/05/2018
ms.keywords: WMPFolderScanState, WMPFolderScanState enumeration [Windows Media Player], wmp.wmpfolderscanstate, wmp/WMPFolderScanState, wmp/wmpfssScanning, wmp/wmpfssStopped, wmp/wmpfssUnknown, wmp/wmpfssUpdating, wmpfssScanning, wmpfssStopped, wmpfssUnknown, wmpfssUpdating
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
targetos: Windows
req.typenames: WMPFolderScanState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPFolderScanState
 - wmp/WMPFolderScanState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPFolderScanState
---

# WMPFolderScanState enumeration


## -description

The <b>WMPFolderScanState</b> enumeration type defines the possible operational states of Windows Media Player as it monitors file folders for digital media content.

## -enum-fields

### -field wmpfssUnknown:0

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

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange">IWMPEvents3::FolderScanStateChange</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate">IWMPFolderMonitorServices::get_scanState</a>
