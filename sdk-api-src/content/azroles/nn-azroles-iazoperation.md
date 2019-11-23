---
UID: NN:azroles.IAzOperation
title: IAzOperation (azroles.h)

description: Defines a low-level operation supported by an application.
old-location: security\iazoperation.htm
tech.root: SecAuthZ
ms.assetid: 054fa4aa-70be-4618-a635-3941c830ea4e

ms.date: 12/05/2018
ms.keywords: IAzOperation, IAzOperation interface [Security], IAzOperation interface [Security],described, azroles/IAzOperation, security.iazoperation
ms.topic: interface
f1_keywords: 
 - "azroles/IAzOperation"
dev_langs:
 - c++
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
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
 - IAzOperation
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzOperation interface


## -description


The <b>IAzOperation</b> interface defines a low-level operation supported by an application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzOperation</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzOperation</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzOperation</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-submit">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzOperation</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzOperation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-get_applicationdata">ApplicationData</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an opaque field that can be used by the application to store information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-get_name">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-get_operationid">OperationID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an application-specific value that uniquely identifies the operation  within the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-get_writable">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the operation can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

