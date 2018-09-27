---
UID: NC:winwlx.PWLX_SAS_NOTIFY
title: PWLX_SAS_NOTIFY
author: windows-sdk-content
description: Called by GINA to notify Winlogon of a secure attention sequence (SAS) event.
old-location: security\wlxsasnotify.htm
tech.root: secauthn
ms.assetid: 534afdf8-6809-413a-ac5c-23978f2b288a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: PWLX_SAS_NOTIFY, PWLX_SAS_NOTIFY callback, WLX_SAS_TYPE_CTRL_ALT_DEL, WlxSasNotify, WlxSasNotify callback function [Security], _gina_wlxsasnotify, security.wlxsasnotify, winwlx/WlxSasNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxSasNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_SAS_NOTIFY callback function


## -description


<p class="CCE_Message">[The WlxSasNotify function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to notify <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS) event.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param dwSasType [in]

Specifies the type of SAS that occurred. 




Values from zero to WLX_SAS_TYPE_MAX_MSFT_VALUE are reserved to define standard Microsoft SAS types. GINA developers can use values greater than WLX_SAS_TYPE_MAX_MSFT_VALUE to define additional SAS types.

The following values are predefined.

This value will be delivered to one of the GINA SAS service routines called by Winlogon (<a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a>, 
<a href="https://msdn.microsoft.com/d60d1464-1948-444c-801a-dde17905091b">WlxLoggedOnSAS</a>, or 
<a href="https://msdn.microsoft.com/7a9f8b00-857a-432e-bb49-2251504c46a0">WlxWkstaLockedSAS</a>).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_CTRL_ALT_DEL"></a><a id="wlx_sas_type_ctrl_alt_del"></a><dl>
<dt><b>WLX_SAS_TYPE_CTRL_ALT_DEL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the user has typed the CTRL+ALT+DEL SAS.

</td>
</tr>
</table>
 


## -returns



This function has no return values.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/d60d1464-1948-444c-801a-dde17905091b">WlxLoggedOnSAS</a>



<a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a>



<a href="https://msdn.microsoft.com/7a9f8b00-857a-432e-bb49-2251504c46a0">WlxWkstaLockedSAS</a>
 

 

