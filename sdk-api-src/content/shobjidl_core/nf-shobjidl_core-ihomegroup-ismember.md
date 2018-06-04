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

# IHomeGroup::IsMember


## -description


Determines whether the local computer is a member of a HomeGroup.


## -parameters




### -param member [out]

Type: <b>BOOL*</b>

When this method returns successfully, receives <b>TRUE</b> if the local computer is a member of a HomeGroup; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The following code snippet shows how to create an instance of <a href="https://msdn.microsoft.com/97d693c0-1126-4cd3-8aee-b5499b538403">IHomeGroup</a> and call <b>IHomeGroup::IsMember</b>.
         
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#include "shobjidl.h"
#include "atlbase.h"   // For COM smart pointers
                    
CComPtr&lt;IHomeGroup&gt; spHomeGroup;
HRESULT hr = S_OK;
BOOL fIsHGMember = FALSE;

// Initialize the COM subsystem.
hr = CoInitialize(NULL);
if (FAILED(hr)) return hr;

// Create an instance of IHomeGroup.
hr = CoCreateInstance(CLSID_HomeGroup, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&amp;spHomeGroup));

if (FAILED(hr)) return hr;

// fIsHGMember receives the value TRUE if the local computer is a member of a 
// HomeGroup, or FALSE if the computer is not a HomeGroup member.
hr = spHomeGroup-&gt;IsMember(&amp;fIsHGMember);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="22d9ea8d-ed66-4c34-940f-141db11e83bd">CComPtr</a>



<a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a>



<a href="https://msdn.microsoft.com/97d693c0-1126-4cd3-8aee-b5499b538403">IHomeGroup</a>
 

 

