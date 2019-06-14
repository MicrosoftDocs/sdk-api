---
UID: NN:windows.foundation.IStringable
title: IStringable (windows.foundation.h)
author: windows-sdk-content
description: Provides a way to represent the current object as a string.
old-location: winrt\istringable.htm
tech.root: WinRT
ms.assetid: 1D67D073-57E8-4562-8586-CAF2619995D7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStringable, IStringable interface [Windows Runtime], IStringable interface [Windows Runtime],described, windows/IStringable, winrt.istringable
ms.topic: interface
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - COM
api_location:
 - windows.foundation.h
api_name:
 - IStringable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStringable interface


## -description


Provides a way to represent the current object as a string. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringable</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IStringable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStringable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-istringable-tostring">ToString</a>
</td>
<td align="left" width="63%">
Gets a string that represents the current object.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Important</b>  Managed types should not implement the <b>IStringable</b> interface. For more info, see <a href="http://go.microsoft.com/fwlink/p/?LinkID=85776">Object.ToString Method</a>.</div>
<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

