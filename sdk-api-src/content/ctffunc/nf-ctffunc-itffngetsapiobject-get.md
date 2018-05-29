---
UID: NF:ctffunc.ITfFnGetSAPIObject.Get
title: ITfFnGetSAPIObject::Get
author: windows-sdk-content
description: ITfFnGetSAPIObject::Get method
old-location: tsf\itffngetsapiobject_get.htm
old-project: TSF
ms.assetid: 4dfa2bd2-e25c-4481-ab07-2f764434504d
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: Get, Get method [Text Services Framework], Get method [Text Services Framework],ITfFnGetSAPIObject interface, ITfFnGetSAPIObject interface [Text Services Framework],Get method, ITfFnGetSAPIObject.Get, ITfFnGetSAPIObject::Get, _tsf_itffngetsapiobject_get_ref, ctffunc/ITfFnGetSAPIObject::Get, tsf.itffngetsapiobject_get
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfFnGetSAPIObject.Get
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnGetSAPIObject::Get


## -description




## -parameters




### -param sObj [in]

Contains a <a href="https://msdn.microsoft.com/82fb6417-efee-4f04-a9a9-4e52934e2e86">TfSapiObject</a> value that specifies the SAPI object to obtain.


### -param ppunk [out]

Pointer to an <b>IUnknown</b> interface pointer that receives the requested SAPI object. The caller must release this interface when it is no longer required.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested object cannot be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The requested object is not implemented.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d7b4caa5-e915-4e57-878a-2a2d6ce609a7">ITfFnGetSAPIObject</a>



<a href="https://msdn.microsoft.com/82fb6417-efee-4f04-a9a9-4e52934e2e86">TfSapiObject
      </a>
 

 

