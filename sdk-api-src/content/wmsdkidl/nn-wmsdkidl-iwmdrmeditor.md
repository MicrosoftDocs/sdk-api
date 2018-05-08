---
UID: NN:wmsdkidl.IWMDRMEditor
title: IWMDRMEditor
author: windows-driver-content
description: The IWMDRMEditor interface is exposed on the metadata editor object.
old-location: wmformat\iwmdrmeditor.htm
old-project: wmformat
ms.assetid: a404d30d-0b42-44c9-93e6-3eb9ef9e40fc
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMDRMEditor, IWMDRMEditor interface [windows Media Format], IWMDRMEditor interface [windows Media Format],described, IWMDRMEditorInterface, wmformat.iwmdrmeditor, wmsdkidl/IWMDRMEditor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMDRMEditor
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMEditor interface


## -description


<p class="CCE_Message">[<b>IWMDRMEditor</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMEditor</b> interface is exposed on the metadata editor object. It can be obtained by calling <b>QueryInterface</b> from <a href="https://msdn.microsoft.com/ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66">IWMMetadataEditor</a>. The <b>IWMDRMEditor</b> interface enables applications to examine the <a href="wmformat_glossary.htm">DRM</a> attributes of an ASF file, for example to query the number of times a file is allowed to be played, without having the wmstubdrm.lib static library. The <a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader</a> interface contains a similar method, but the application must be linked to a valid wmstubdrm.lib library in order to use that interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMEditor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDRMEditor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMEditor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0a7b07d-f0c0-4715-a9c3-7babf3bf7af9">GetDRMProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified DRM property or file attribute.

</td>
</tr>
</table> 

For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/86ee18be-38a9-4f76-810c-e33281df8c23">IWMDRMReader::GetDRMProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>



<a href="https://msdn.microsoft.com/fbfa1a1b-afd0-4f61-86ae-488716e16355">Viewing Attributes of Protected Files</a>
 

 

