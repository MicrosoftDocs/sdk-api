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

# IWbemStatusCodeText::GetFacilityCodeText


## -description


The 
    <b>IWbemStatusCodeText::GetFacilityCodeText</b> 
    method returns the name of the subsystem where the error occurred, such as "Windows", "WBEM", "SSPI", or "RPC".


## -parameters




### -param hRes [in]

Handle to the error code for which you want a description.


### -param LocaleId [in]

Reserved. This parameter must be 0 (zero).


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param MessageText [out]

Pointer to a string containing the descriptive text of the error code.


## -returns



This method returns <b>WMI_S_NO_ERROR</b> if successful.




## -remarks



To enable the 
    <b>GetFacilityCodeText</b> method to 
    return the subsystem name, the caller must free the pointer in the <i>MessageText</i> 
    parameter.


#### Examples

The following example describes how to use 
     <b>GetFacilityCodeText</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IWbemStatusCodeText * pStatus = NULL;

    SCODE sc = CoCreateInstance(CLSID_WbemStatusCodeText, 
                                    0, CLSCTX_INPROC_SERVER,
                                    IID_IWbemStatusCodeText,
                                    (LPVOID *) &amp;pStatus);
    
    if(sc == S_OK)
    {
        BSTR bstr = 0;

        // The m_hres is an HRESULT variable that has already
        // been declared and initialized.
        sc = pStatus-&gt;GetErrorCodeText(m_hres, 0, 0, &amp;bstr);
        if(sc == S_OK)
        {
            // ...display string here.
            SysFreeString(bstr);
            bstr = 0;
        }
        sc = pStatus-&gt;GetFacilityCodeText(m_hres, 0, 0, &amp;bstr);
        if(sc == S_OK)
        {
            // to do, display this.
            SysFreeString(bstr);
            bstr = 0;
        }
        pStatus-&gt;Release();
    }

    // clean up.
    pStatus-&gt;Release();</pre>
</td>
</tr>
</table></span></div>


