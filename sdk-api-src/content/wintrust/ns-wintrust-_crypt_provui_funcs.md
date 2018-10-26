---
UID: NS:wintrust._CRYPT_PROVUI_FUNCS
title: "_CRYPT_PROVUI_FUNCS"
author: windows-sdk-content
description: Provides information about the user interface (UI) functions of a provider. This structure is used by the CRYPT_PROVIDER_FUNCTIONS structure.
old-location: security\crypt_provui_funcs.htm
tech.root: seccrypto
ms.assetid: 7cdc32ea-b28a-400f-ad8a-984f86bb95fd
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PCRYPT_PROVUI_FUNCS, CRYPT_PROVUI_FUNCS, CRYPT_PROVUI_FUNCS structure [Security], PCRYPT_PROVUI_FUNCS, PCRYPT_PROVUI_FUNCS structure pointer [Security], _CRYPT_PROVUI_FUNCS, security.crypt_provui_funcs, wintrust/CRYPT_PROVUI_FUNCS, wintrust/PCRYPT_PROVUI_FUNCS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVUI_FUNCS
product: Windows
targetos: Windows
req.typenames: CRYPT_PROVUI_FUNCS, *PCRYPT_PROVUI_FUNCS
req.redist: 
---

# _CRYPT_PROVUI_FUNCS structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_PROVUI_FUNCS</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVUI_FUNCS</b> structure provides information about the user interface (UI) functions of a provider. This structure is used by the  <a href="https://msdn.microsoft.com/2c00f8ec-e262-4df8-8984-a2702a4162bf">CRYPT_PROVIDER_FUNCTIONS</a> structure.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field psUIData

A pointer to a <a href="https://msdn.microsoft.com/86f819f0-c243-45ba-8b7b-97ed906e6e8a">CRYPT_PROVUI_DATA</a> structure.  


### -field pfnOnMoreInfoClick

A pointer to the  function called when the <b>More Info</b> button is clicked.


### -field pfnOnMoreInfoClickDefault

A pointer to the  default function called when the <b>More Info</b> button is clicked.


### -field pfnOnAdvancedClick

A pointer to the  function called when the <b>Advanced</b> button is clicked.


### -field pfnOnAdvancedClickDefault

A pointer to the  default function called when the <b>Advanced</b> button is clicked.


## -remarks



The prototype for PFN_PROVUI_CALL is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Wintrust.h&gt;

typedef BOOL (*PFN_PROVUI_CALL)(
    IN HWND hWndSecurityDialog,
    IN struct _CRYPT_PROVIDER_DATA *pProvData
);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a>



<a href="https://msdn.microsoft.com/2c00f8ec-e262-4df8-8984-a2702a4162bf">CRYPT_PROVIDER_FUNCTIONS</a>
 

 

