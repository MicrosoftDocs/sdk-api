---
UID: NN:inspectable.IInspectable
title: IInspectable
author: windows-sdk-content
description: Provides functionality required for all Windows Runtime classes.
old-location: winrt\iinspectable.htm
tech.root: WinRT
ms.assetid: 0657E51F-D4C0-46C6-927D-B01E54B6846C
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IInspectable, IInspectable interface [Windows Runtime], IInspectable interface [Windows Runtime],described, inspectable/IInspectable, winrt.iinspectable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
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
 - COM
api_location:
 - Inspectable.h
api_name:
 - IInspectable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInspectable interface


## -description


Provides functionality required for all Windows Runtime classes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInspectable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInspectable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInspectable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/560094E6-3ED2-4BF3-85C7-07736ECBACC8">GetIids</a>
</td>
<td align="left" width="63%">
Gets the interfaces that are implemented by the current Windows Runtime class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E0A0B56D-E676-46FD-873D-11309102DFFD">GetRuntimeClassName</a>
</td>
<td align="left" width="63%">
Gets the fully qualified name of the current Windows Runtime object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7E8AFD1-A8B7-4023-9F8B-573E0D2622F6">GetTrustLevel</a>
</td>
<td align="left" width="63%">
Gets the trust level of the current Windows Runtime object.

</td>
</tr>
</table> 


## -remarks



<b>IInspectable</b> methods have no effect on COM apartments and are safe to call from user interface threads.






## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/75E30E4B-EE5F-41C4-AC22-91D542E920EB">TrustLevel</a>
 

 

