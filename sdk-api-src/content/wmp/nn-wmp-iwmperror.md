---
UID: NN:wmp.IWMPError
title: IWMPError (wmp.h)
description: The IWMPError interface provides methods for accessing a collection of IWMPErrorItem pointers.
old-location: wmp\iwmperror.htm
tech.root: WMP
ms.assetid: f22759cd-0ca7-4992-bb17-0272b35d6d75
ms.date: 12/05/2018
ms.keywords: IWMPError, IWMPError interface [Windows Media Player], IWMPError interface [Windows Media Player],described, IWMPErrorInterface, wmp.iwmperror, wmp/IWMPError
f1_keywords:
- wmp/IWMPError
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.h
api_name:
- IWMPError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPError interface


## -description



The <b>IWMPError</b> interface provides methods for accessing a collection of <b>IWMPErrorItem</b> pointers.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPError</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmperror-clearerrorqueue">clearErrorQueue</a>
</td>
<td align="left" width="63%">
Clears the errors from the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmperror-get_errorcount">get_errorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of errors in the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmperror-get_item">get_item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPErrorItem</b> interface at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmperror-webhelp">webHelp</a>
</td>
<td align="left" width="63%">
Launches the Microsoft Windows Media Player Web Help page to display further information about the error.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPError</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_error">get_error</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

