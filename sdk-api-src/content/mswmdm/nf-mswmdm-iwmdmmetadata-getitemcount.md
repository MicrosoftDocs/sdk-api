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

# IWMDMMetaData::GetItemCount


## -description



The <b>GetItemCount</b> method retrieves the total number of properties held by the interface.




## -parameters




### -param iCount [out]

Pointer to an integer that receives the total number of metadata properties stored by the interface.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method could be used along with <a href="https://msdn.microsoft.com/5d27e1e9-ab91-433d-8216-ace195386d44">QueryByIndex</a> to enumerate all properties on a storage or device.


#### Examples

The following code retrieves the count of properties in an <b>IWMDMMetaData</b> interface (pMetadata) and tries to retrieve them all by index and print them. It uses a custom error handling macro BREAK_HR.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
        //
        // Loop through all metadata properties, and print out the value of each.
        //
        BYTE* value;
        WMDM_TAG_DATATYPE type;
        UINT len = 0;
        UINT count = 0;
        WCHAR* name;
        // Get the number of metadata items.
        hr = pMetadata-&gt;GetItemCount(&amp;count);

        BREAK_HR(hr, "Got a metadata count in GetMetadata.", "Couldn't get a metadata count in GetMetadata.");
        for(;count &gt; 0; count--)
        {
            // Get the metadata property by index.
            WCHAR* name;
            hr = pMetadata-&gt;QueryByIndex(count-1, &amp;name, &amp;type, &amp;value, &amp;len);
            if (SUCCEEDED(hr))
            {
                // TODO: Display the property name.
                CoTaskMemFree(name);

                // Print out the value of the property, according to the value type.
                switch (type)
                {
                case WMDM_TYPE_QWORD:
                case WMDM_TYPE_DWORD:
                case WMDM_TYPE_WORD:
                    // TODO: Display the value.
                    break;
                case WMDM_TYPE_STRING:
                    // TODO: Display the value.
                    // Release the method-allocated property value memory.
                    if (SUCCEEDED(hr))
                        CoTaskMemFree(value);
                    break;
                case WMDM_TYPE_BOOL:
                    // TODO: Display the value.
                    break;
                case WMDM_TYPE_BINARY:
                    // TODO: Display the value.
                    break;
                case WMDM_TYPE_DATE:
                    {
                        WMDMDATETIME *val = (WMDMDATETIME*)value;
                        / /TODO: Display the month, day, and year.
                    }
                    break;
                case WMDM_TYPE_GUID:
                    {
                        WCHAR strGuid[64];
                        StringFromGUID2(reinterpret_cast&lt;GUID&amp;&gt;(value),(LPOLESTR)strGuid, 64);
                        / /TODO: Display the GUID.
                    }
                    break;
                default:
                    // TODO: Display a message indicating that the 
                    // application could not understand the returned value type.
                }
            }
            else // Couldn't get the metadata property at index count - 1.
                // TODO: Display a message indicating that the 
                // application couldn't retrieve a value for the index.
        // Clear the WMDM-allocated memory.
        if (value)
            CoTaskMemFree(value);
        }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>



<a href="https://msdn.microsoft.com/5d27e1e9-ab91-433d-8216-ace195386d44">QueryByIndex</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

