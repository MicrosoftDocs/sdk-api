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

# IEnumPortableDeviceObjectIDs::Next


## -description



        The <b>Next</b> method retrieves the next one or more object IDs in the enumeration sequence.
      


## -parameters




### -param cObjects [in]


            A count of the objects requested.
          


### -param pObjIDs [in, out]


            An array of <b>LPWSTR</b> pointers, each specifying a retrieved object ID. The caller must allocate an array of <i>cObjects</i> LPWSTR elements. The caller must free both the array and the returned strings. The strings are freed by calling <a href="4fe971c6-8611-453d-b69b-f02c17cf17d4">CoTaskMemFree</a>.
          


### -param pcFetched [in, out]


            On input, this parameter is ignored. On output, the number of IDs actually retrieved. If no object IDs are released and the return value is S_FALSE, there are no more objects to enumerate.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more objects to enumerate.

</td>
</tr>
</table>
 




## -remarks




        If fewer than the requested number of elements remain in the sequence, this method retrieves the remaining elements. The number of elements that are actually retrieved is returned through <i>pcFetched</i> (unless the caller passed in NULL for that parameter). Enumerated objects are all peers—that is, enumerating children of an object will enumerate only direct children, not grandchild or deeper objects.
      


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// This number controls how many object identifiers are requested during each call
// to IEnumPortableDeviceObjectIDs::Next()
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(LPCWSTR wszParentObjectID, IPortableDeviceContent* pContent)
{
    HRESULT                       hr             = S_OK;
    IEnumPortableDeviceObjectIDs* pEnumObjectIDs = NULL;

    if ((wszParentObjectID == NULL) ||
        (pContent          == NULL))
    {
        return;
    }

    // wszParentObjectID is the object identifier of the parent being used for enumeration

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    hr = pContent-&gt;EnumObjects(0, wszParentObjectID, NULL, &amp;pEnumObjectIDs);
    if (FAILED(hr))
    {
        // Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        LPWSTR szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs-&gt;Next(NUM_OBJECTS_TO_REQUEST, // Number of objects to request on each NEXT call
                                  szObjectIDArray,        // Array of LPWSTR array which will be populated on each NEXT call
                                  &amp;cFetched);             // Number of objects written to the LPWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex &lt; cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated LPWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }

    // Release the IEnumPortableDeviceObjectIDs when finished
    if (pEnumObjectIDs != NULL)
    {
        pEnumObjectIDs-&gt;Release();
        pEnumObjectIDs = NULL;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/86782a09-4fca-4ae0-beaf-296069e061dc">Enumerating Content</a>



<a href="https://msdn.microsoft.com/0e9a65cc-819c-494e-9c7c-8f5fec78a2ee">IEnumPortableDeviceObjectIDs Interface</a>
 

 

