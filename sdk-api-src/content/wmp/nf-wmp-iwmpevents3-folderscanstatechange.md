---
UID: NF:wmp.IWMPEvents3.FolderScanStateChange
title: IWMPEvents3::FolderScanStateChange
author: windows-sdk-content
description: The FolderScanStateChange event occurs when a folder monitoring operation changes state.
old-location: wmp\iwmpevents3_iwmpevents3__folderscanstatechange.htm
tech.root: WMP
ms.assetid: 07e9a49b-19a6-4ed2-b037-fe44ada920a1
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FolderScanStateChange, FolderScanStateChange method [Windows Media Player], FolderScanStateChange method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],FolderScanStateChange method, IWMPEvents3.FolderScanStateChange, IWMPEvents3::FolderScanStateChange, IWMPEvents3FolderScanStateChange, wmp.iwmpevents3_iwmpevents3__folderscanstatechange, wmp/IWMPEvents3::FolderScanStateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents3.FolderScanStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents3::FolderScanStateChange


## -description



The <b>FolderScanStateChange</b> event occurs when a folder monitoring operation changes state.




## -parameters




### -param wmpfss [in]

<b>WMPFolderScanState</b> enumeration value that indicates the new state.


## -returns



This method does not return a value.




## -remarks



You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/20909420-5f90-4334-b21a-82d6cdc6d019">WMPFolderScanState</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

