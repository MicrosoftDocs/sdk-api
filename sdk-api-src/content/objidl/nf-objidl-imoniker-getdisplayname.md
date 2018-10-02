---
UID: NF:objidl.IMoniker.GetDisplayName
title: IMoniker::GetDisplayName
author: windows-sdk-content
description: Retrieves the display name for the moniker.
old-location: com\imoniker_getdisplayname.htm
tech.root: com
ms.assetid: 424036c9-c097-4507-b562-4a01f9199b1f
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetDisplayName, GetDisplayName method [COM], GetDisplayName method [COM],IMoniker interface, IMoniker interface [COM],GetDisplayName method, IMoniker.GetDisplayName, IMoniker::GetDisplayName, _com_imoniker_getdisplayname, com.imoniker_getdisplayname, objidl/IMoniker::GetDisplayName
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMoniker.GetDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMoniker::GetDisplayName


## -description


Retrieves the display name for the moniker.


## -parameters




### -param pbc [in]

A pointer to the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on the bind context to be used in this operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.


### -param pmkToLeft [in]

If the moniker is part of a composite moniker, pointer to the moniker to the left of this moniker. This parameter is used primarily by moniker implementers to enable cooperation between the various components of a composite moniker. Moniker clients should pass <b>NULL</b>.


### -param ppszDisplayName [out]

The address of a pointer variable that receives a pointer to the display name string for the moniker. The implementation must use <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a> to allocate the string returned in <i>ppszDisplayName</i>, and the caller is responsible for calling <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a> to free it. Both the caller and the implementation of this method use the COM task allocator returned by <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>. If an error occurs, the implementation must set *<i>ppszDisplayName</i> should be set to <b>NULL</b>.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_EXCEEDEDDEADLINE</b></dt>
</dl>
</td>
<td width="60%">
The binding operation could not be completed within the time limit specified by the bind context's <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
There is no display name.

</td>
</tr>
</table>
 




## -remarks



<b>GetDisplayName</b> provides a string that is a displayable representation of the moniker. A display name is not a complete representation of a moniker's internal state; it is simply a form that can be read by users. As a result, it is possible (though rare) for two different monikers to have the same display name. While there is no guarantee that the display name of a moniker can be parsed back into that moniker when calling the <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> function with it, failure to do so is rare.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
It is possible that retrieving a moniker's display name may be an expensive operation. For efficiency, you may want to cache the results of the first successful call to <b>GetDisplayName</b>, rather than making repeated calls.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you are writing a moniker class in which the display name does not change, simply cache the display name and supply the cached name when requested. If the display name can change over time, getting the current display name might mean that the moniker has to access the object's storage or bind to the object, either of which can be expensive operations. If this is the case, your implementation of <b>GetDisplayName</b> should return MK_E_EXCEEDEDDEADLINE if the name cannot be retrieved by the time specified in the bind context's <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure.

A moniker that is intended to be part of a generic composite moniker should include any preceding delimiter (such as '\') as part of its display name. For example, the display name returned by an item moniker includes the delimiter specified when it was created with the <a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a> function. The display name for a file moniker does not include a delimiter because file monikers are always expected to be the leftmost component of a composite.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>For each anti-moniker contained in this moniker, this method return one instance of "\..".</td>
</tr>
<tr>
<td>Class moniker</td>
<td>The display name for class monikers is of the following form: clsid:<i>string-clsid-no-curly-braces</i> *[";" <i>clsid-param</i>=<i>value</i>]:. For example, clsid:a7b90590-36fd-11cf-857d-00aa006d2ea4:.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns the path that the moniker represents.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method returns the concatenation of the display names returned by each component moniker of the composite.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns the concatenation of the delimiter and the item name that were specified when the item moniker was created.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method obtains the display name for the OBJREF moniker. The display name is a 64-bit encoding that encapsulates the machine location, process endpoint, and interface pointer ID (IPID) of the running object. For future compatibility, the display name is restricted to characters that can be specified as part of a URL.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>The URL moniker attempts to return its full URL string. If the moniker was created with a partial URL string (see <a href="https://msdn.microsoft.com/library/ms775103(v=VS.85).aspx">CreateURLMonikerEx</a>), it will first attempt to find an URL moniker in the bind context under SZ_URLCONTEXT and will next look to the moniker to its left for contextual information. If it cannot return its full URL string, it will return its partial URL string.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>
 

 

