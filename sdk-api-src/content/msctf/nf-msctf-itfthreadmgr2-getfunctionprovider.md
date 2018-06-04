---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# ITfThreadMgr2::GetFunctionProvider


## -description


 Obtains the specified function provider object.


## -parameters




### -param clsid [in]

CLSID of the desired function provider. This can be the CLSID of a function provider registered for the calling thread or one of the following predefined values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_SYSTEM_FUNCTIONPROVIDER"></a><a id="guid_system_functionprovider"></a><dl>
<dt><b>GUID_SYSTEM_FUNCTIONPROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Obtains the TSF system function provider.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_APP_FUNCTIONPROVIDER"></a><a id="guid_app_functionprovider"></a><dl>
<dt><b>GUID_APP_FUNCTIONPROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Obtains the function provider implemented by the current application. This object is not available if the application does not register itself as a function provider.

</td>
</tr>
</table>
 


### -param ppFuncProv [out]

Pointer to a <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> interface that receives the function provider.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOPROVIDER</b></dt>
</dl>
</td>
<td width="60%">
No function provider matching <i>clsid</i> was available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
GUID_SYSTEM_FUNCTIONPROVIDER was requested, but cannot be obtained.

</td>
</tr>
</table>
 




## -remarks



A function provider registers by calling the TSF manager <a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink</a> method with IID_ITfFunctionProvider.




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

