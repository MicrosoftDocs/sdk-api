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
 

 

