---
UID: NF:objidl.IMoniker.CommonPrefixWith
title: IMoniker::CommonPrefixWith (objidl.h)
description: Creates a new moniker based on the prefix that this moniker has in common with the specified moniker.
helpviewer_keywords: ["CommonPrefixWith","CommonPrefixWith method [COM]","CommonPrefixWith method [COM]","IMoniker interface","IMoniker interface [COM]","CommonPrefixWith method","IMoniker.CommonPrefixWith","IMoniker::CommonPrefixWith","_com_imoniker_commonprefixwith","com.imoniker_commonprefixwith","objidl/IMoniker::CommonPrefixWith"]
old-location: com\imoniker_commonprefixwith.htm
tech.root: com
ms.assetid: ef2a3191-7b7c-4e51-ab55-cf601f444561
ms.date: 12/05/2018
ms.keywords: CommonPrefixWith, CommonPrefixWith method [COM], CommonPrefixWith method [COM],IMoniker interface, IMoniker interface [COM],CommonPrefixWith method, IMoniker.CommonPrefixWith, IMoniker::CommonPrefixWith, _com_imoniker_commonprefixwith, com.imoniker_commonprefixwith, objidl/IMoniker::CommonPrefixWith
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMoniker::CommonPrefixWith
 - objidl/IMoniker::CommonPrefixWith
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMoniker.CommonPrefixWith
---

# IMoniker::CommonPrefixWith


## -description

Creates a new moniker based on the prefix that this moniker has in common with the specified moniker.

## -parameters

### -param pmkOther [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on another moniker to be compared with this one to determine whether there is a common prefix.

### -param ppmkPrefix [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the moniker that is the common prefix of this moniker and pmkOther. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the resulting moniker; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs or if there is no common prefix, the implementation should set *<i>ppmkPrefix</i> to <b>NULL</b>.

## -returns

This method can return the standard return values E_OUTOFMEMORY, as well as the following values.

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
A common prefix exists that is neither this moniker nor <i>pmkOther</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_NOPREFIX</b></dt>
</dl>
</td>
<td width="60%">
No common prefix exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_HIM</b></dt>
</dl>
</td>
<td width="60%">
The entire <i>pmkOther</i> is a prefix of this moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_US</b></dt>
</dl>
</td>
<td width="60%">
The two monikers are identical.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_ME</b></dt>
</dl>
</td>
<td width="60%">
This moniker is a prefix of the <i>pmkOther</i> moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_NOTBINDABLE</b></dt>
</dl>
</td>
<td width="60%">
This method was called on a relative moniker. It is not meaningful to take the common prefix on a relative moniker.

</td>
</tr>
</table>

## -remarks

<b>CommonPrefixWith</b> creates a new moniker that consists of the common prefixes of the moniker on this moniker object and another moniker. For example, if one moniker represents the path "c:\projects\secret\art\pict1.bmp" and another moniker represents the path "c:\projects\secret\docs\chap1.txt", the common prefix of these two monikers would be a moniker representing the path "c:\projects\secret".

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <b>CommonPrefixWith</b> method is primarily called in the implementation of the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-relativepathto">IMoniker::RelativePathTo</a> method. Clients using a moniker to locate an object rarely need to call this method.



Call this method only if <i>pmkOther</i> and this moniker are both absolute monikers. An absolute moniker is either a file moniker or a generic composite whose leftmost component is a file moniker that represents an absolute path. Do not call this method on relative monikers because it would not produce meaningful results.



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation should first determine whether <i>pmkOther</i> is a moniker of a class that you recognize and for which you can provide special handling (for example, if it is of the same class as this moniker). If so, your implementation should determine the common prefix of the two monikers. Otherwise, it should pass both monikers in a call to the <a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a> function, which correctly handles the generic case. 


<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>
If the other moniker is also an anti-moniker, the method returns MK_S_US and sets ppmkPrefix to this moniker. Otherwise, the method calls the <a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a> function. This function correctly handles the case where the other moniker is a generic composite.

</td>
</tr>
<tr>
<td>Class moniker</td>
<td>
If <i>pmkOther</i> is equal to this moniker, retrieves a pointer to this moniker and returns MK_S_US. If <i>pmkOther</i> is a class moniker but is not equal to this moniker, returns MK_E_NOPREFIX. Otherwise, returns the result of calling <a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a> with itself as <i>pmkThis</i>, <i>pmkOther</i>, and <i>ppmkPrefix</i>, which handles the case where <i>pmkOther</i> is a generic composite moniker.

</td>
</tr>
<tr>
<td>File moniker</td>
<td>
If both monikers are file monikers, this method returns a file moniker that is based on the common components at the beginning of two file monikers. Components of a file moniker can be of the following types:

<ul>
<li>A computer name of the form \\server\share. A computer name is treated as a single component, so two monikers representing the paths "\\myserver\public\work" and "\\myserver\private\games" do not have "\\myserver" as a common prefix.</li>
<li>A drive designation (for example, "C:").</li>
<li>A directory or file name.</li>
</ul>
If the other moniker is not a file moniker, this method passes both monikers in a call to the <a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a> function. This function correctly handles the case where the other moniker is a generic composite.

This method returns MK_E_NOPREFIX if there is no common prefix.

</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>
If the other moniker is a composite, this method compares the components of each composite from left to right. The returned common prefix moniker might also be a composite moniker, depending on how many of the leftmost components were common to both monikers. If the other moniker is not a composite, the method simply compares it to the leftmost component of this moniker.

If the monikers are equal, the method returns MK_S_US and sets <i>ppmkPrefix</i> to this moniker. If the other moniker is a prefix of this moniker, the method returns MK_S_HIM and sets <i>ppmkPrefix</i> to the other moniker. If this moniker is a prefix of the other, this method returns MK_S_ME and sets <i>ppmkPrefix</i> to this moniker.

If there is no common prefix, this method returns MK_E_NOPREFIX and sets <i>ppmkPrefix</i> to <b>NULL</b>.

</td>
</tr>
<tr>
<td>Item moniker</td>
<td>
If the other moniker is an item moniker that is equal to this moniker, this method sets *<i>ppmkPrefix</i> to this moniker and returns MK_S_US; otherwise, the method calls the <a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a> function. This function correctly handles the case where the other moniker is a generic composite.

</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>
If the two monikers are equal, this method returns MK_S_US and sets *<i>ppmkPrefix</i> to <b>NULL</b>. If the other moniker is not an OBJREF moniker, this method passes both monikers to the <a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a> function. This function correctly handles the case where the other moniker is a generic composite.

If there is no common prefix, this method returns MK_E_NOPREFIX.

</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>
If the two monikers are equal, this method returns MK_S_US and sets *<i>ppmkPrefix</i> to this moniker. Otherwise, the method returns MK_E_NOPREFIX and sets *<i>ppmkPrefix</i> to <b>NULL</b>.

</td>
</tr>
<tr>
<td>URL moniker</td>
<td>
This method returns E_NOTIMPL.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objbase/nf-objbase-monikercommonprefixwith">MonikerCommonPrefixWith</a>