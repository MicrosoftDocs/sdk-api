---
UID: NS:wia_xp._WIA_EXTENDED_TRANSFER_INFO
title: "_WIA_EXTENDED_TRANSFER_INFO"
author: windows-sdk-content
description: The WIA_EXTENDED_TRANSFER_INFO structure specifies extended transfer information for the IWiaDataTransfer::idtGetExtendedTransferInfo method.
old-location: wia\_wia_WIA_EXTENDED_TRANSFER_INFO.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_extended_transfer_info.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PWIA_EXTENDED_TRANSFER_INFO, PWIA_EXTENDED_TRANSFER_INFO, PWIA_EXTENDED_TRANSFER_INFO structure pointer [WIA], WIA_EXTENDED_TRANSFER_INFO, WIA_EXTENDED_TRANSFER_INFO structure [WIA], _WIA_EXTENDED_TRANSFER_INFO, _wia_WIA_EXTENDED_TRANSFER_INFO, wia._wia_WIA_EXTENDED_TRANSFER_INFO, wia_xp/PWIA_EXTENDED_TRANSFER_INFO, wia_xp/WIA_EXTENDED_TRANSFER_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WIA_EXTENDED_TRANSFER_INFO, *PWIA_EXTENDED_TRANSFER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wia_xp.h
api_name:
 - WIA_EXTENDED_TRANSFER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WIA_EXTENDED_TRANSFER_INFO structure


## -description


The <b>WIA_EXTENDED_TRANSFER_INFO</b> structure specifies extended transfer information for the <a href="https://msdn.microsoft.com/en-us/library/ms630153(v=VS.85).aspx">IWiaDataTransfer::idtGetExtendedTransferInfo</a> method.


## -struct-fields




### -field ulSize

Type: <b>ULONG</b>

Size of this structure.



### -field ulMinBufferSize

Type: <b>ULONG</b>

Minimum buffer size the application should request in a call to <a href="https://msdn.microsoft.com/en-us/library/ms630151(v=VS.85).aspx">IWiaDataTransfer::idtGetBandedData</a>.


### -field ulOptimalBufferSize

Type: <b>ULONG</b>

Driver-recommended buffer size the application should request in a call to <a href="https://msdn.microsoft.com/en-us/library/ms630151(v=VS.85).aspx">IWiaDataTransfer::idtGetBandedData</a>.


### -field ulMaxBufferSize

Type: <b>ULONG</b>

Driver-recommended maximum buffer size the application could request in a call to <a href="https://msdn.microsoft.com/en-us/library/ms630151(v=VS.85).aspx">IWiaDataTransfer::idtGetBandedData</a>. Going over this limit is not detrimental, however, the driver can simply not use the whole buffer and limit each band of data to this maximum size.


### -field ulNumBuffers

Type: <b>ULONG</b>

This value is not used and should be ignored.

