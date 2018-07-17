---
UID: NF:strmif.IFilterMapper2.EnumMatchingFilters
title: IFilterMapper2::EnumMatchingFilters
author: windows-sdk-content
description: The EnumMatchingFilters method enumerates registered filters that meet specified requirements.
old-location: dshow\ifiltermapper2_enummatchingfilters.htm
old-project: DirectShow
ms.assetid: f121b4c3-fce1-4be3-ace4-5084242130f6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: EnumMatchingFilters, EnumMatchingFilters method [DirectShow], EnumMatchingFilters method [DirectShow],IFilterMapper2 interface, IFilterMapper2 interface [DirectShow],EnumMatchingFilters method, IFilterMapper2.EnumMatchingFilters, IFilterMapper2::EnumMatchingFilters, IFilterMapper2EnumMatchingFilters, dshow.ifiltermapper2_enummatchingfilters, strmif/IFilterMapper2::EnumMatchingFilters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2.EnumMatchingFilters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper2::EnumMatchingFilters


## -description



The <code>EnumMatchingFilters</code> method enumerates registered filters that meet specified requirements.




## -parameters




### -param ppEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a> interface. Use this interface pointer to retrieve filter monikers from the enumeration. The caller must release the interface.


### -param dwFlags [in]

Reserved, must be zero.


### -param bExactMatch [in]

Boolean value indicating whether an exact match is required. See Remarks for more information.


### -param dwMerit [in]

Minimum merit value. The enumeration exludes filters with a lesser merit value. For a list of merit values, see <a href="https://msdn.microsoft.com/9e026675-e0a9-4c82-9b57-ab0e7d9592ea">Merit</a>. If <i>dwMerit</i> is higher than MERIT_DO_NOT_USE, the enumeration also excludes filters whose category has a merit less than or equal to MERIT_DO_NOT_USE. (See <a href="https://msdn.microsoft.com/cab4e2c9-eab9-4836-adfc-870490ca5b6b">Filter Categories</a>.)


### -param bInputNeeded [in]

Boolean value indicating whether the filter must have an input pin. If the value is <b>TRUE</b>, the filter must have at least one input pin.


### -param cInputTypes [in]

Number of input media types specified in <i>pInputTypes</i>.


### -param pInputTypes [in]

Pointer to an array of GUID pairs that specify major types and subtypes, for the input pins to match. The size of the array is 2 * <i>cInputTypes</i>. The array can be <b>NULL</b>. Individual array members can be GUID_NULL, which matches any type. (See <a href="https://msdn.microsoft.com/c8efe9e6-7d1d-4ec2-ab1b-70ee0798a6a3">Media Types</a>.)


### -param pMedIn [in]

Pointer to a <a href="https://msdn.microsoft.com/ed5614fe-bfeb-4ddf-a626-b14080f45b33">REGPINMEDIUM</a> structure specifying the medium for the input pins. Set to <b>NULL</b> if not needed.


### -param pPinCategoryIn [in]

Pointer to a GUID that specifies the input pin category. (See <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a>.) Set to <b>NULL</b> if not needed.


### -param bRender [in]

Boolean value that specifies whether the filter must render its input. If <b>TRUE</b>, the specified filter must render its input. (This value corresponds to the <b>bRendered</b> field in the <a href="https://msdn.microsoft.com/1da033e1-24c3-46e0-becf-025966e6238f">REGFILTERPINS</a> structure, which is used to register information about the filter's pins.)


### -param bOutputNeeded [in]

Boolean value specifying whether the filter must have an output pin. If <b>TRUE</b>, the filter must have at least one output pin.


### -param cOutputTypes [in]

Number of input media types specified in <i>pOutputTypes</i>.


### -param pOutputTypes [in]

Pointer to an array of GUID pairs that specify major types and subtypes, for the output pins to match. The size of the array is 2 * <i>cOutputTypes</i>. The array can be <b>NULL</b>. Individual array members can be GUID_NULL, which matches any type.


### -param pMedOut [in]

Pointer to a <a href="https://msdn.microsoft.com/ed5614fe-bfeb-4ddf-a626-b14080f45b33">REGPINMEDIUM</a> structure specifying the medium for the output pins. Set to <b>NULL</b> if not needed.


### -param pPinCategoryOut [in]

Pointer to a GUID that specifies the output pin category. (See <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a>.) Set to <b>NULL</b> if not needed.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>
 




## -remarks



To find filters whose input pins match a given set of media types, declare an array with major-type GUIDs and subtype GUIDs ordered in pairs. Pass the array address in the <i>pInputTypes</i> parameter, and set the <i>cInputTypes</i> parameter equal to the number of pairs (that is, half the array size):

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = GUID_NULL;

DWORD cInTypes = 1;
</pre>
</td>
</tr>
</table></span></div>
For output pins, pass a similar array in the <i>pOutputTypes</i> parameter, and specify the number of GUID pairs in the <i>cOutputTypes</i> parameter.

If the value of the <i>bExactMatch</i> parameter is <b>TRUE</b>, this method looks for filters that exactly match the values you specify for media type, pin category, and pin medium. If the value is <b>FALSE</b>, filters that register a value of <b>NULL</b> for any of these items are considered a match. (In effect, a <b>NULL</b> value in the registry acts as a wildcard.)

If you specify <b>NULL</b> for media type, pin category, or pin medium, any filter is considered a match for that parameter.

If a pin did not register any media types, this method will not consider it a match for the media type.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2 Interface</a>
 

 

