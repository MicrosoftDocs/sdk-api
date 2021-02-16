---
UID: NF:wbemcli.IWbemStatusCodeText.GetFacilityCodeText
title: IWbemStatusCodeText::GetFacilityCodeText (wbemcli.h)
description: The IWbemStatusCodeText::GetFacilityCodeText method returns the name of the subsystem where the error occurred, such as &quot;Windows&quot;, &quot;WBEM&quot;, &quot;SSPI&quot;, or &quot;RPC&quot;.
helpviewer_keywords: ["GetFacilityCodeText","GetFacilityCodeText method [Windows Management Instrumentation]","GetFacilityCodeText method [Windows Management Instrumentation]","IWbemStatusCodeText interface","IWbemStatusCodeText interface [Windows Management Instrumentation]","GetFacilityCodeText method","IWbemStatusCodeText.GetFacilityCodeText","IWbemStatusCodeText::GetFacilityCodeText","_hmm_iwbemstatuscodetext_getfacilitycodetext","wbemcli/IWbemStatusCodeText::GetFacilityCodeText","wmi.iwbemstatuscodetext_getfacilitycodetext"]
old-location: wmi\iwbemstatuscodetext_getfacilitycodetext.htm
tech.root: wmi
ms.assetid: 831f8eb4-3dcd-42ec-aa43-309360e9a5ce
ms.date: 12/05/2018
ms.keywords: GetFacilityCodeText, GetFacilityCodeText method [Windows Management Instrumentation], GetFacilityCodeText method [Windows Management Instrumentation],IWbemStatusCodeText interface, IWbemStatusCodeText interface [Windows Management Instrumentation],GetFacilityCodeText method, IWbemStatusCodeText.GetFacilityCodeText, IWbemStatusCodeText::GetFacilityCodeText, _hmm_iwbemstatuscodetext_getfacilitycodetext, wbemcli/IWbemStatusCodeText::GetFacilityCodeText, wmi.iwbemstatuscodetext_getfacilitycodetext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemStatusCodeText::GetFacilityCodeText
 - wbemcli/IWbemStatusCodeText::GetFacilityCodeText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemStatusCodeText.GetFacilityCodeText
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


```cpp
IWbemStatusCodeText * pStatus = NULL;

    SCODE sc = CoCreateInstance(CLSID_WbemStatusCodeText, 
                                    0, CLSCTX_INPROC_SERVER,
                                    IID_IWbemStatusCodeText,
                                    (LPVOID *) &pStatus);
    
    if(sc == S_OK)
    {
        BSTR bstr = 0;

        // The m_hres is an HRESULT variable that has already
        // been declared and initialized.
        sc = pStatus->GetErrorCodeText(m_hres, 0, 0, &bstr);
        if(sc == S_OK)
        {
            // ...display string here.
            SysFreeString(bstr);
            bstr = 0;
        }
        sc = pStatus->GetFacilityCodeText(m_hres, 0, 0, &bstr);
        if(sc == S_OK)
        {
            // to do, display this.
            SysFreeString(bstr);
            bstr = 0;
        }
        pStatus->Release();
    }

    // clean up.
    pStatus->Release();
```

