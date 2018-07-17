---
UID: NN:msctf.ITfDisplayAttributeProvider
title: ITfDisplayAttributeProvider
author: windows-sdk-content
description: The ITfDisplayAttributeProvider interface is implemented by a text service and is used by the TSF manager to enumerate and obtain individual display attribute information objects.
old-location: tsf\itfdisplayattributeprovider.htm
old-project: TSF
ms.assetid: c0346d5e-d4a2-4c72-90be-de5ff1681acd
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfDisplayAttributeProvider, ITfDisplayAttributeProvider interface [Text Services Framework], ITfDisplayAttributeProvider interface [Text Services Framework],described, _tsf_itfdisplayattributeprovider_ref, msctf/ITfDisplayAttributeProvider, tsf.itfdisplayattributeprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imjpcic.dll
api_name:
 - ITfDisplayAttributeProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: Imjpcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDisplayAttributeProvider interface


## -description


The <b>ITfDisplayAttributeProvider</b> interface is implemented by a text service and is used by the TSF manager to enumerate and obtain individual display attribute information objects.

The TSF manager obtains an instance of this interface by calling <a href="_com_cocreateinstance">CoCreateInstance</a> with the class identifier passed to <a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">ITfCategoryMgr::RegisterCategory</a> with GUID_TFCAT_DISPLAYATTRIBUTEPROVIDER and IID_ITfDisplayAttributeProvider. For more information, see <a href="https://msdn.microsoft.com/5809f5b8-0396-4abd-b5fe-61ecc8cd0914">Providing Display Attributes</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfDisplayAttributeProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDisplayAttributeProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a19de91-ad79-4c75-956b-5f5de6700cbe">EnumDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all display attribute info objects supported by the display attribute provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2081f1b4-45b4-43bd-ba20-392a5ad0a30e">GetDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains a display attribute provider object for a particular display attribute.

</td>
</tr>
</table> 


## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">ITfCategoryMgr::RegisterCategory
      </a>



<a href="_COM_IUnknown">IUnknown</a>



<a href="https://msdn.microsoft.com/5809f5b8-0396-4abd-b5fe-61ecc8cd0914">Providing Display Attributes</a>
 

 

