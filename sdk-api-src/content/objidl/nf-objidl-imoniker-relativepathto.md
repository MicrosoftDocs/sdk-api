---
UID: NF:objidl.IMoniker.RelativePathTo
title: IMoniker::RelativePathTo
author: windows-sdk-content
description: Creates a relative moniker between this moniker and the specified moniker.
old-location: com\imoniker_relativepathto.htm
tech.root: com
ms.assetid: 92e2e7d7-043e-4e95-8540-5a895b5a54f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMoniker interface [COM],RelativePathTo method, IMoniker.RelativePathTo, IMoniker::RelativePathTo, RelativePathTo, RelativePathTo method [COM], RelativePathTo method [COM],IMoniker interface, _com_imoniker_relativepathto, com.imoniker_relativepathto, objidl/IMoniker::RelativePathTo
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IMoniker.RelativePathTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMoniker::RelativePathTo


## -description


Creates a relative moniker between this moniker and the specified moniker.


## -parameters




### -param pmkOther [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the moniker to which a relative path should be taken.


### -param ppmkRelPath [out]

A pointer to an  <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> pointer variable that receives the interface pointer to the relative moniker. When successful, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the new moniker; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs, the implementation sets *<i>ppmkRelPath</i> to <b>NULL</b>.


## -returns



This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_HIM</b></dt>
</dl>
</td>
<td width="60%">
No common prefix is shared by the two monikers and the moniker returned in <i>ppmkRelPath</i> is <i>pmkOther</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOTBINDABLE</b></dt>
</dl>
</td>
<td width="60%">
This moniker is a relative moniker, such as an item moniker. This moniker must be composed with the moniker of its container before a relative path can be determined.

</td>
</tr>
</table>
 




## -remarks



A relative moniker is analogous to a relative path (such as "..\backup"). For example, suppose you have one moniker that represents the path "c:\projects\secret\art\pict1.bmp" and another moniker that represents the path "c:\projects\secret\docs\chap1.txt". Calling <b>RelativePathTo</b> on the first moniker, passing the second one as the <i>pmkOther</i> parameter, would create a relative moniker representing the path "..\docs\chap1.txt".

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Moniker clients typically do not need to call <b>RelativePathTo</b>. This method is called primarily by the default handler for linked objects. Linked objects contain both an absolute and a relative moniker to identify the link source. (This enables link tracking if the user moves a directory tree containing both the container and source files.) The default handler calls this method to create a relative moniker from the container document to the link source. (That is, it calls <b>RelativePathTo</b> on the moniker identifying the container document, passing the moniker identifying the link source as the <i>pmkOther</i> parameter.)

If you do call <b>RelativePathTo</b>, call it only on absolute monikersâ€”for example, a file moniker or a composite moniker whose leftmost component is a file moniker, where the file moniker represents an absolute path. Do not call this method on relative monikers.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>RelativePathTo</b> should first determine whether <i>pmkOther</i> is a moniker of a class that you recognize and for which you can provide special handling (for example, if it is of the same class as this moniker). If so, your implementation should determine the relative path. Otherwise, it should pass both monikers in a call to the <a href="https://msdn.microsoft.com/55ab4db3-a94e-48ba-abe3-44963c35e062">MonikerRelativePathTo</a> function, which correctly handles the generic case.

The first step in determining a relative path is determining the common prefix of this moniker and <i>pmkOther</i>. The next step is to break this moniker and <i>pmkOther</i> into two parts each, say (P, myTail) and (P, otherTail) respectively, where P is the common prefix. The correct relative path is then the inverse of myTail composed with otherTail:

Comp( Inv( myTail ), otherTail )

where Comp() represents the composition operation and Inv() represents the inverse operation.

For certain types of monikers, you cannot use your <a href="https://msdn.microsoft.com/351d5da3-043b-426a-99e9-9f882f552239">IMoniker::Inverse</a> method to construct the inverse of myTail. For example, a file moniker returns an anti-moniker as an inverse, while its <b>RelativePathTo</b> method must use one or more file monikers that each represent the path ".." to construct the inverse of myTail.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns MK_S_HIM and sets *<i>ppmkRelPath</i> to the other moniker.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns the result of calling <a href="https://msdn.microsoft.com/55ab4db3-a94e-48ba-abe3-44963c35e062">MonikerRelativePathTo</a> with <i>pmkSrc</i> equal to this moniker, <i>pmkOther</i>, <i>ppmkRelPath</i>, and <b>TRUE</b> as <i>dwReserved</i>.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method computes a moniker which when composed to the right of this moniker yields the other moniker. For example, if the path of this moniker is "C:\work\docs\report.doc" and if the other moniker is "C:\work\art\picture.bmp", the path of the computed moniker would be "..\..\art\picture.bmp". </td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method finds the common prefix of the two monikers and creates two monikers that consist of the remainder when the common prefix is removed. Then it creates the inverse for the remainder of this moniker and composes the remainder of the other moniker on the right of it.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns MK_E_NOTBINDABLE and sets *<i>ppmkRelPath</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/55ab4db3-a94e-48ba-abe3-44963c35e062">MonikerRelativePathTo</a>
 

 

