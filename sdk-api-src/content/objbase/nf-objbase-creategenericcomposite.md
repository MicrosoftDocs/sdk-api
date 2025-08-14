---
UID: NF:objbase.CreateGenericComposite
title: CreateGenericComposite function (objbase.h)
description: Performs a generic composition of two monikers and supplies a pointer to the resulting composite moniker.
helpviewer_keywords: ["CreateGenericComposite","CreateGenericComposite function [COM]","_com_CreateGenericComposite","com.creategenericcomposite","objbase/CreateGenericComposite"]
old-location: com\creategenericcomposite.htm
tech.root: com
ms.assetid: 7fe5b3ff-6e9b-4a28-93d3-52c76d3e8b77
ms.date: 12/05/2018
ms.keywords: CreateGenericComposite, CreateGenericComposite function [COM], _com_CreateGenericComposite, com.creategenericcomposite, objbase/CreateGenericComposite
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateGenericComposite
 - objbase/CreateGenericComposite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
 - CreateGenericComposite
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# CreateGenericComposite function


## -description

Performs a generic composition of two monikers and supplies a pointer to the resulting composite moniker.

## -parameters

### -param pmkFirst [in, optional]

A pointer to the moniker to be composed to the left of the moniker that pmkRest points to. Can point to any kind of moniker, including a generic composite.

### -param pmkRest [in, optional]

A pointer to the moniker to be composed to the right of the moniker to which <i>pmkFirst</i> points. Can point to any kind of moniker compatible with the type of the <i>pmkRest</i> moniker, including a generic composite.

### -param ppmkComposite [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the composite moniker object that is the result of composing <i>pmkFirst</i> and <i>pmkRest</i>. This object supports the OLE composite moniker implementation of <b>IMoniker</b>. When successful, the function has called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the moniker and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If either <i>pmkFirst</i> or <i>pmkRest</i> are <b>NULL</b>, the supplied pointer is the one that is non-<b>NULL</b>. If both <i>pmkFirst</i> and <i>pmkRest</i> are <b>NULL</b>, or if an error occurs, the returned pointer is <b>NULL</b>.

## -returns

This function can return the standard return value E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The input monikers were composed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The two monikers could not be composed due to an error in the syntax of a path (for example, if both pmkFirst and pmkRest are file monikers based on absolute paths).

</td>
</tr>
</table>

## -remarks

<b>CreateGenericComposite</b> joins two monikers into one. The moniker classes being joined can be different, subject only to the rules of composition. Call this function only if you are writing a new moniker class by implementing the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface, within an implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">IMoniker::ComposeWith</a> that includes generic composition capability.

Moniker providers should call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">ComposeWith</a> to compose two monikers together. Implementations of <b>ComposeWith</b> should (as do OLE implementations) attempt, when reasonable for the class, to perform non-generic compositions first, in which two monikers of the same class are combined. If this is not possible, the implementation can call <b>CreateGenericComposite</b> to do a generic composition, which combines two monikers of different classes, within the rules of composition. You can define new types of non-generic compositions if you write a new moniker class.

During the process of composing the two monikers, <b>CreateGenericComposite</b> makes all possible simplifications. Consider the example where <i>pmkFirst</i> is the generic composite moniker, A + B + C, and <i>pmkRest</i> is the generic composite moniker, C -1 + B -1 + Z (where C -1 is the inverse of C). The function first composes C to C -1, which composes to nothing. Then it composes B and B -1 to nothing. Finally, it composes A to Z, and supplies a pointer to the generic composite moniker, A + Z.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">IMoniker::ComposeWith</a>
