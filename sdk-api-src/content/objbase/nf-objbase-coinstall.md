---
UID: NF:objbase.CoInstall
title: CoInstall function
author: windows-sdk-content
description: Installs the requested COM server application.
old-location: com\coinstall.htm
old-project: com
ms.assetid: 9486ef2d-51a1-41b4-85e5-427af9a98cec
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoInstall, CoInstall function [COM], _com_CoInstall, com.coinstall, objbase/CoInstall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoInstall
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CoInstall function


## -description


Installs the requested COM server application. 


## -parameters




### -param pbc [in]

This parameter is reserved and must be <b>NULL</b>.


### -param dwFlags [in]

This parameter is reserved and must be 0.


### -param pClassSpec [in]

A pointer to a uCLSSPEC structure. The <b>tyspec</b> member must be set to TYSPEC_CLSID and the <b>clsid</b> member must be set to the CLSID to be installed. For more information see <a href="https://msdn.microsoft.com/f2972300-5a95-43e3-b2d1-cd8f30d14d1d">TYSPEC</a>.


### -param pQuery [in]

A pointer to a <a href="https://msdn.microsoft.com/5d6a17e1-dcdd-4691-aec2-f63dbcb26027">QUERYCONTEXT</a> structure. The <b>dwContext</b> member must be set to the desired <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> value.


### -param pszCodeBase [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This function can return the standard return value E_INVALIDARG, as well as the following values.

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
<dt><b>CS_E_PACKAGE_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>tyspec</b> member of <i>pClassSpec</i> was not set to TYSPEC_CLSID.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5d6a17e1-dcdd-4691-aec2-f63dbcb26027">QUERYCONTEXT</a>



<a href="https://msdn.microsoft.com/f2972300-5a95-43e3-b2d1-cd8f30d14d1d">TYSPEC</a>
 

 

