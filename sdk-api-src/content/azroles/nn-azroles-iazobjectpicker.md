---
UID: NN:azroles.IAzObjectPicker
title: IAzObjectPicker (azroles.h)
author: windows-sdk-content
description: Displays a dialog box that allows users to select one or more principals from a list.
old-location: security\iazobjectpicker.htm
tech.root: SecAuthZ
ms.assetid: 767f30c9-6071-4f04-876d-b8b2392e650c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzObjectPicker, IAzObjectPicker interface [Security], IAzObjectPicker interface [Security],described, azroles/IAzObjectPicker, security.iazobjectpicker
ms.topic: interface
f1_keywords: 
 - "azroles/IAzObjectPicker"
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzObjectPicker
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzObjectPicker interface


## -description


The <b>IAzObjectPicker</b> interface displays a dialog box that allows users to select one or more principals from a list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzObjectPicker</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzObjectPicker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzObjectPicker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazobjectpicker-getprincipals">GetPrincipals</a>
</td>
<td align="left" width="63%">
Displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzObjectPicker</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazobjectpicker-get_name">Name</a>


</td>
<td align="left" width="63%">
Gets the name of the <b>IAzObjectPicker</b> object.

</td>
</tr>
</table> 


## -remarks



Implement this interface when you need a custom dialog box that allows users to choose principals.



