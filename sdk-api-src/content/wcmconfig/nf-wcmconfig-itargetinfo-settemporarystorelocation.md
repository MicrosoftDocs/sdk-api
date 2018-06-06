---
UID: NF:wcmconfig.ITargetInfo.SetTemporaryStoreLocation
title: ITargetInfo::SetTemporaryStoreLocation
author: windows-sdk-content
description: Sets the current temporary store location.
old-location: smi\itargetinfo_settemporarystorelocation.htm
old-project: SMI
ms.assetid: ef2b6983-02ff-488a-99ef-9976d76f51b5
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ITargetInfo interface [SMI],SetTemporaryStoreLocation method, ITargetInfo.SetTemporaryStoreLocation, ITargetInfo::SetTemporaryStoreLocation, SetTemporaryStoreLocation, SetTemporaryStoreLocation method [SMI], SetTemporaryStoreLocation method [SMI],ITargetInfo interface, smi.itargetinfo_settemporarystorelocation, wcmconfig/ITargetInfo::SetTemporaryStoreLocation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.SetTemporaryStoreLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

