---
UID: NF:wbemcli.IWbemStatusCodeText.GetErrorCodeText
title: IWbemStatusCodeText::GetErrorCodeText
author: windows-sdk-content
description: Returns the text string description associated with the error code.
old-location: wmi\iwbemstatuscodetext_geterrorcodetext.htm
old-project: WmiSdk
ms.assetid: f2adc740-f1d9-434e-a7ac-b4830350e862
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetErrorCodeText, GetErrorCodeText method [Windows Management Instrumentation], GetErrorCodeText method [Windows Management Instrumentation],IWbemStatusCodeText interface, IWbemStatusCodeText interface [Windows Management Instrumentation],GetErrorCodeText method, IWbemStatusCodeText.GetErrorCodeText, IWbemStatusCodeText::GetErrorCodeText, _hmm_iwbemstatuscodetext_geterrorcodetext, wbemcli/IWbemStatusCodeText::GetErrorCodeText, wmi.iwbemstatuscodetext_geterrorcodetext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemStatusCodeText.GetErrorCodeText
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemStatusCodeText::GetErrorCodeText


## -description


The 
   <b>IWbemStatusCodeText::GetErrorCodeText</b> 
   method returns the text string description associated with the error code.


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



This method returns <b>WBEM_S_NO_ERROR</b> if successful.




## -remarks



To enable <b>GetErrorCodeText</b> to 
    return the text string description, the caller must free the pointer in the <i>MessageText</i> 
    parameter.


#### Examples

The following example describes how to implement 
<b>GetErrorCodeText</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IWbemStatusCodeText * pStatus = NULL;

    SCODE sc = CoCreateInstance(CLSID_WbemStatusCodeText,
                                0, 
                                CLSCTX_INPROC_SERVER,
                                IID_IWbemStatusCodeText,
                                (LPVOID *) &amp;pStatus);
    
    if(sc == S_OK)
    {
        BSTR bstr = 0;

        // The m_hres isan HRESULT variable that has already
        // been declared and initialized.
        sc = pStatus-&gt;GetErrorCodeText(m_hres, 0, 0, &amp;bstr);
        if(sc == S_OK)
        {
            // to do, display this:
            SysFreeString(bstr);
            bstr = 0;
        }
        sc = pStatus-&gt;GetFacilityCodeText(m_hres, 0, 0, &amp;bstr);
        if(sc == S_OK)
        {
            // to do, display this:
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


