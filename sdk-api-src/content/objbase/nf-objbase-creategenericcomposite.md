---
UID: NF:objbase.CreateGenericComposite
title: CreateGenericComposite function
author: windows-sdk-content
description: Performs a generic composition of two monikers and supplies a pointer to the resulting composite moniker.
old-location: com\creategenericcomposite.htm
old-project: com
ms.assetid: 7fe5b3ff-6e9b-4a28-93d3-52c76d3e8b77
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateGenericComposite, CreateGenericComposite function [COM], _com_CreateGenericComposite, com.creategenericcomposite, objbase/CreateGenericComposite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: objbase.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
 - CreateGenericComposite
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
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

The address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>* pointer variable that receives the interface pointer to the composite moniker object that is the result of composing <i>pmkFirst</i> and <i>pmkRest</i>. This object supports the OLE composite moniker implementation of <b>IMoniker</b>. When successful, the function has called <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the moniker and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If either <i>pmkFirst</i> or <i>pmkRest</i> are <b>NULL</b>, the supplied pointer is the one that is non-<b>NULL</b>. If both <i>pmkFirst</i> and <i>pmkRest</i> are <b>NULL</b>, or if an error occurs, the returned pointer is <b>NULL</b>.


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



<b>CreateGenericComposite</b> joins two monikers into one. The moniker classes being joined can be different, subject only to the rules of composition. Call this function only if you are writing a new moniker class by implementing the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface, within an implementation of <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a> that includes generic composition capability.

Moniker providers should call <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">ComposeWith</a> to compose two monikers together. Implementations of <b>ComposeWith</b> should (as do OLE implementations) attempt, when reasonable for the class, to perform non-generic compositions first, in which two monikers of the same class are combined. If this is not possible, the implementation can call <b>CreateGenericComposite</b> to do a generic composition, which combines two monikers of different classes, within the rules of composition. You can define new types of non-generic compositions if you write a new moniker class.

During the process of composing the two monikers, <b>CreateGenericComposite</b> makes all possible simplifications. Consider the example where <i>pmkFirst</i> is the generic composite moniker, A + B + C, and <i>pmkRest</i> is the generic composite moniker, C -1 + B -1 + Z (where C -1 is the inverse of C). The function first composes C to C -1, which composes to nothing. Then it composes B and B -1 to nothing. Finally, it composes A to Z, and supplies a pointer to the generic composite moniker, A + Z.





## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a>
 

 

