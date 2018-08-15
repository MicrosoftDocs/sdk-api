---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnCurrentCellularClassChange
title: IMbnMultiCarrierEvents::OnCurrentCellularClassChange
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a GetCurrentCellularClass operation.
old-location: mbn\imbnmulticarrierevents_oncurrentcellularclasschange.htm
old-project: mbn
ms.assetid: 76B5349E-EA51-422D-81BC-A93B85FBCF90
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnCurrentCellularClassChange method, IMbnMultiCarrierEvents.OnCurrentCellularClassChange, IMbnMultiCarrierEvents::OnCurrentCellularClassChange, OnCurrentCellularClassChange, OnCurrentCellularClassChange method [Microsoft Broadband Networks], OnCurrentCellularClassChange method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, mbn.imbnmulticarrierevents_oncurrentcellularclasschange, mbnapi/IMbnMultiCarrierEvents::OnCurrentCellularClassChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrierEvents.OnCurrentCellularClassChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnMultiCarrierEvents::OnCurrentCellularClassChange


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/8DA29C25-3866-4BCA-8591-F8408A1C1401">GetCurrentCellularClass</a> operation.


## -parameters




### -param mbnInterface [in]

An <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object that represents the Mobile Broadband device <a href="https://msdn.microsoft.com/8DA29C25-3866-4BCA-8591-F8408A1C1401">GetCurrentCellularClass</a> operation.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation  was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>
 

 

