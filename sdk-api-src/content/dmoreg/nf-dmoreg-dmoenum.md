---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DMOEnum function


## -description


The <b>DMOEnum</b> function enumerates DMOs listed in the registry. The caller can search by category, media type, or both.


## -parameters




### -param guidCategory

GUID that specifies which category of DMO to search. Use GUID_NULL to search every category. See <a href="https://msdn.microsoft.com/d67debd0-8ecb-41ab-bc6c-b27cba97c65a">DMO GUIDs</a> for a list of category GUIDs.


### -param dwFlags

Bitwise combination of zero or more flags from the DMO_ENUM_FLAGS enumeration.


### -param cInTypes

Number of input media types to use in the search criteria. Use zero to match any input type.




### -param pInTypes

Pointer to an array of <a href="https://msdn.microsoft.com/53bf4c34-d180-4edd-b59a-55d7d90708b5">DMO_PARTIAL_MEDIATYPE</a> structures that contain the input media types. Specify the size of the array in the cInTypes parameter.


### -param cOutTypes

Number of output media types to use in the search criteria. Use zero to match any output type.


### -param pOutTypes

Pointer to an array of DMO_PARTIAL_MEDIATYPE structures that contain the output media types. Specify the size of the array in the cOutTypes parameter. 


### -param ppEnum

Address of a variable to receive the <a href="https://msdn.microsoft.com/221248f2-5c8f-442e-a6ad-e0372ddc1aae">IEnumDMO</a> interface of the enumerator.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



This method returns a pointer to an enumerator object that supports the <a href="https://msdn.microsoft.com/221248f2-5c8f-442e-a6ad-e0372ddc1aae">IEnumDMO</a> interface. The application uses the <b>IEnumDMO</b> interface to enumerate over the set of DMOs that match the search criteria.


#### Examples

The following example enumerates all audio effect DMOs on the user's system, including keyed DMOs.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IEnumDMO* pEnum = NULL; 
HRESULT hr = DMOEnum(
    DMOCATEGORY_AUDIO_EFFECT, // Category
    DMO_ENUMF_INCLUDE_KEYED,  // Included keyed DMOs
    0, NULL,                  // Input types (don't care)
    0, NULL,                  // Output types (don't care)
    &amp;pEnum);

if (SUCCEEDED(hr)) 
{
    CLSID clsidDMO;
    WCHAR* wszName;
    do
    {
        hr = pEnum-&gt;Next(1, &amp;clsidDMO, &amp;wszName, NULL);
        if (hr == S_OK) 
        {  
            // Now wszName holds the friendly name of the DMO, 
            // and clsidDMO holds the CLSID. 

            // Remember to release wszName!
            CoTaskMemFree(wszName);
        }
    } while (hr == S_OK);
    pEnum-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0a380dc0-23f0-4ef0-898a-3b5afddf5eaa">DMO Functions</a>
 

 

