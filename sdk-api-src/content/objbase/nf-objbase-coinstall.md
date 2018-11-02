---
UID: NF:objbase.CoInstall
title: CoInstall function
author: windows-sdk-content
description: Installs the requested COM server application.
old-location: winprog\coinstall.htm
tech.root: devnotes
ms.assetid: 92b290a5-0923-42fc-8231-1decca26adc1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CoInstall, CoInstall function [Windows API], objbase/CoInstall, winprog.coinstall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# CoInstall function


## -description


<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Installs the requested COM server application.


## -parameters




### -param pbc [in]

Reserved for future use; this value must be <b>NULL</b>.


### -param dwFlags [in]

Reserved for future use; this value must be 0.


### -param pClassSpec [in]

A pointer to a <b>uCLSSPEC</b> union. The <b>tyspec</b> member must be set to TYSPEC_CLSID and the <b>clsid</b> member must be set to the CLSID to be installed. For more information, see <a href="https://msdn.microsoft.com/1af170e3-1edd-411f-acba-d4b244107996">TYSPEC</a>.


### -param pQuery [in]

A pointer to a <a href="https://msdn.microsoft.com/8b27c090-2bae-4511-9be8-4bc077295ac5">QUERYCONTEXT</a> structure. The <b>dwContext</b> field must be set to the desired <a href="_com_CLSCTX">CLSCTX</a> value. For more information, see <b>QUERYCONTEXT</b>.


### -param pszCodeBase

TBD




#### - pszCodeName [in]

Reserved for future use; this value must be <b>NULL</b>.


## -returns



This function supports the standard return value E_INVALIDARG, as well as the following.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="S_OK"></a><a id="s_ok"></a>S_OK

</td>
<td width="60%">
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<a id="CS_E_PACKAGE_NOTFOUND"></a><a id="cs_e_package_notfound"></a>CS_E_PACKAGE_NOTFOUND

</td>
<td width="60%">
The <b>tyspec</b> field of <i>pClassSpec</i> was not set to TYSPEC_CLSID.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8b27c090-2bae-4511-9be8-4bc077295ac5">QUERYCONTEXT</a>



<a href="https://msdn.microsoft.com/1af170e3-1edd-411f-acba-d4b244107996">TYSPEC</a>
 

 

