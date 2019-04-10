---
UID: NN:ctffunc.ITfFnConfigure
title: ITfFnConfigure (ctffunc.h)
author: windows-sdk-content
description: The ITfFnConfigure interface is implemented by a text service to enable the Text Services control panel application to allow the text service to display a configuration dialog box.
old-location: tsf\itffnconfigure.htm
tech.root: TSF
ms.assetid: af23e668-9c00-4e53-89b6-c8be85ae961b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnConfigure, ITfFnConfigure interface [Text Services Framework], ITfFnConfigure interface [Text Services Framework],described, _tsf_itffnconfigure_ref, ctffunc/ITfFnConfigure, tsf.itffnconfigure
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfFnConfigure
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnConfigure interface


## -description


The <b>ITfFnConfigure</b> interface is implemented by a text service to enable the Text Services control panel application to allow the text service to display a configuration dialog box.

The Text Services control panel application obtains an instance of this interface by calling <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with the class identifier passed to <a href="https://msdn.microsoft.com/264bc32e-60a2-4dff-a212-5682d30a769e">ITfInputProcessorProfiles::Register</a> and IID_ITfFnConfigure.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnConfigure</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnConfigure</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnConfigure</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34670748-460b-4ece-b742-83b0cf87d901">Show</a>
</td>
<td align="left" width="63%">
Called when the user opens the Text Services control panel application, selects the text service from the list and presses the Properties pushbutton.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction
      </a>



<a href="https://msdn.microsoft.com/264bc32e-60a2-4dff-a212-5682d30a769e">ITfInputProcessorProfiles::Register
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

