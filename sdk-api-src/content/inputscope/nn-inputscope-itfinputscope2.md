---
UID: NN:inputscope.ITfInputScope2
title: ITfInputScope2
author: windows-driver-content
description: The ITfInputScope2 interface is used by the text input processors to get the IEnumString interface pointer and this IEnumString interface enumerates the word list that the application specified for this context.
old-location: tsf\ITfInputScope2.htm
old-project: TSF
ms.assetid: 45314d3a-cb54-4524-819a-16c035dfe533
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfInputScope2, ITfInputScope2 interface [Text Services Framework], ITfInputScope2 interface [Text Services Framework],described, _tsf_itfinputscope2_ref, inputscope/ITfInputScope2, tsf.ITfInputScope2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InputScope
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfInputScope2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputScope2 interface


## -description


The <b>ITfInputScope2</b> interface is used by the text input processors to get the IEnumString interface pointer and this IEnumString interface enumerates the word list that the application specified for this context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputScope2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfInputScope2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputScope2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89379dab-6f96-4a86-8433-b6b0a8e45516">EnumWordList</a>
</td>
<td align="left" width="63%">
Return a pointer to obtain the IEnumString interface pointer.

</td>
</tr>
</table> 

