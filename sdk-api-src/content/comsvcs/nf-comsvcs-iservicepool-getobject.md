---
UID: NF:comsvcs.IServicePool.GetObject
title: IServicePool::GetObject
author: windows-sdk-content
description: Retrieves an object from the object pool.
old-location: cos\iservicepool_getobject.htm
tech.root: cossdk
ms.assetid: f1b9487a-156c-4c2c-ab18-edfd66d96315
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetObject, GetObject method [COM+], GetObject method [COM+],IServicePool interface, IServicePool interface [COM+],GetObject method, IServicePool.GetObject, IServicePool::GetObject, _cos_IServicePool_GetObject, comsvcs/IServicePool::GetObject, cos.iservicepool_getobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP4, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePool.GetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServicePool::GetObject


## -description


Retrieves an object from the object pool.

The object returned is a COM object that can run under arbitrary threading models and contexts.


## -parameters




### -param riid [in]

A reference to the identifier of the object requested.


### -param ppv [out]

The requested object.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ACTIVATION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Object activation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ACTIVATIONFAILED_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Object activation failed due to time-out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object pool was not initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fb86ffa5-b4cd-48bc-a99e-245e75ddb9c2">IServicePool</a>
 

 

