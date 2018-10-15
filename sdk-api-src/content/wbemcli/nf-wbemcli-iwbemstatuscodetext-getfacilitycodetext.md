---
UID: NF:wbemcli.IWbemStatusCodeText.GetFacilityCodeText
title: IWbemStatusCodeText::GetFacilityCodeText
author: windows-sdk-content
description: The IWbemStatusCodeText::GetFacilityCodeText method returns the name of the subsystem where the error occurred, such as &#0034;Windows&#0034;, &#0034;WBEM&#0034;, &#0034;SSPI&#0034;, or &#0034;RPC&#0034;.
old-location: wmi\iwbemstatuscodetext_getfacilitycodetext.htm
tech.root: WmiSdk
ms.assetid: 831f8eb4-3dcd-42ec-aa43-309360e9a5ce
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetFacilityCodeText, GetFacilityCodeText method [Windows Management Instrumentation], GetFacilityCodeText method [Windows Management Instrumentation],IWbemStatusCodeText interface, IWbemStatusCodeText interface [Windows Management Instrumentation],GetFacilityCodeText method, IWbemStatusCodeText.GetFacilityCodeText, IWbemStatusCodeText::GetFacilityCodeText, _hmm_iwbemstatuscodetext_getfacilitycodetext, wbemcli/IWbemStatusCodeText::GetFacilityCodeText, wmi.iwbemstatuscodetext_getfacilitycodetext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemStatusCodeText.GetFacilityCodeText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


