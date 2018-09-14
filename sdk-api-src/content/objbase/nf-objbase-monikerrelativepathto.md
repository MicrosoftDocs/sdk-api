---
UID: NF:objbase.MonikerRelativePathTo
title: MonikerRelativePathTo function
author: windows-sdk-content
description: Provides a moniker that, when composed onto the end of the first specified moniker (or one with a similar structure), yields the second specified moniker.
old-location: com\monikerrelativepathto.htm
tech.root: com
ms.assetid: 55ab4db3-a94e-48ba-abe3-44963c35e062
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: MonikerRelativePathTo, MonikerRelativePathTo function [COM], _com_MonikerRelativePathTo, com.monikerrelativepathto, objbase/MonikerRelativePathTo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
 - MonikerRelativePathTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonikerRelativePathTo function


## -description


Provides a moniker that, when composed onto the end of the first specified moniker (or one with a similar structure), yields the second specified moniker.

This function is intended for use only by <a href="https://msdn.microsoft.com/92e2e7d7-043e-4e95-8540-5a895b5a54f9">IMoniker::RelativePathTo</a> implementations.


## -parameters




### -param pmkSrc [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the moniker that, when composed with the relative moniker to be created, produces <i>pmkDest</i>. This moniker identifies the "source" of the relative moniker to be created.


### -param pmkDest [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the moniker to be expressed relative to <i>pmkSrc</i>. This moniker identifies the destination of the relative moniker to be created.


### -param ppmkRelPath [out]

The address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>* pointer variable that receives the interface pointer to the new relative moniker. When successful, the function has called <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the moniker and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs, the interface pointer value is <b>NULL</b>.


### -param dwReserved [in]

This parameter is reserved and must be nonzero.


## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
A meaningful relative path has been returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_HIM</b></dt>
</dl>
</td>
<td width="60%">
The only form of the relative path is the other moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOTBINDABLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pmkSrc</i> parameter is a relative moniker, such as an item moniker, and must be composed with the moniker of its container before a relative path can be determined.

</td>
</tr>
</table>
 




## -remarks



Your implementation of <a href="https://msdn.microsoft.com/92e2e7d7-043e-4e95-8540-5a895b5a54f9">IMoniker::RelativePathTo</a> should first check whether the other moniker is of a type you recognize and handle in a special way. If not, you should call <b>MonikerRelativePathTo</b>, passing itself as <i>pmkThis</i> and the other moniker as <i>pmkOther</i>. <b>MonikerRelativePathTo</b> correctly handles the cases where either moniker is a generic composite.



You should call this function only if <i>pmkSrc</i> and <i>pmkDest</i> are both absolute monikers, where an absolute moniker is either a file moniker or a generic composite whose leftmost component is a file moniker, and where the file moniker represents an absolute path. Do not call this function on relative monikers.





## -see-also




<a href="https://msdn.microsoft.com/92e2e7d7-043e-4e95-8540-5a895b5a54f9">IMoniker::RelativePathTo</a>
 

 

