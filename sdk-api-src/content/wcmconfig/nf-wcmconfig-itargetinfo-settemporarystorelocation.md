---
UID: NF:wcmconfig.ITargetInfo.SetTemporaryStoreLocation
title: ITargetInfo::SetTemporaryStoreLocation (wcmconfig.h)
author: windows-sdk-content
description: Sets the current temporary store location.
old-location: smi\itargetinfo_settemporarystorelocation.htm
tech.root: SMI
ms.assetid: ef2b6983-02ff-488a-99ef-9976d76f51b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetTemporaryStoreLocation method, ITargetInfo.SetTemporaryStoreLocation, ITargetInfo::SetTemporaryStoreLocation, SetTemporaryStoreLocation, SetTemporaryStoreLocation method [SMI], SetTemporaryStoreLocation method [SMI],ITargetInfo interface, smi.itargetinfo_settemporarystorelocation, wcmconfig/ITargetInfo::SetTemporaryStoreLocation
ms.topic: method
f1_keywords: 
 - "wcmconfig/ITargetInfo.SetTemporaryStoreLocation"
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.SetTemporaryStoreLocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITargetInfo::SetTemporaryStoreLocation


## -description


Sets the current temporary store location.


## -parameters




### -param TemporaryStoreLocation [in]

The current temporary store location.


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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the target processor architecture has already been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
</td>
<td width="60%">
Indicates that system resources are low.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>
 

 

