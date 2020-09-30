---
UID: NF:wbemcli.IWbemStatusCodeText.GetErrorCodeText
title: IWbemStatusCodeText::GetErrorCodeText (wbemcli.h)
description: Returns the text string description associated with the error code.
helpviewer_keywords: ["GetErrorCodeText","GetErrorCodeText method [Windows Management Instrumentation]","GetErrorCodeText method [Windows Management Instrumentation]","IWbemStatusCodeText interface","IWbemStatusCodeText interface [Windows Management Instrumentation]","GetErrorCodeText method","IWbemStatusCodeText.GetErrorCodeText","IWbemStatusCodeText::GetErrorCodeText","_hmm_iwbemstatuscodetext_geterrorcodetext","wbemcli/IWbemStatusCodeText::GetErrorCodeText","wmi.iwbemstatuscodetext_geterrorcodetext"]
old-location: wmi\iwbemstatuscodetext_geterrorcodetext.htm
tech.root: wmi
ms.assetid: f2adc740-f1d9-434e-a7ac-b4830350e862
ms.date: 12/05/2018
ms.keywords: GetErrorCodeText, GetErrorCodeText method [Windows Management Instrumentation], GetErrorCodeText method [Windows Management Instrumentation],IWbemStatusCodeText interface, IWbemStatusCodeText interface [Windows Management Instrumentation],GetErrorCodeText method, IWbemStatusCodeText.GetErrorCodeText, IWbemStatusCodeText::GetErrorCodeText, _hmm_iwbemstatuscodetext_geterrorcodetext, wbemcli/IWbemStatusCodeText::GetErrorCodeText, wmi.iwbemstatuscodetext_geterrorcodetext
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
 - IWbemStatusCodeText::GetErrorCodeText
 - wbemcli/IWbemStatusCodeText::GetErrorCodeText
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
 - IWbemStatusCodeText.GetErrorCodeText
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


```cpp
IWbemStatusCodeText * pStatus = NULL;

    SCODE sc = CoCreateInstance(CLSID_WbemStatusCodeText,
                                0, 
                                CLSCTX_INPROC_SERVER,
                                IID_IWbemStatusCodeText,
                                (LPVOID *) &pStatus);
    
    if(sc == S_OK)
    {
        BSTR bstr = 0;

        // The m_hres isan HRESULT variable that has already
        // been declared and initialized.
        sc = pStatus->GetErrorCodeText(m_hres, 0, 0, &bstr);
        if(sc == S_OK)
        {
            // to do, display this:
            SysFreeString(bstr);
            bstr = 0;
        }
        sc = pStatus->GetFacilityCodeText(m_hres, 0, 0, &bstr);
        if(sc == S_OK)
        {
            // to do, display this:
            SysFreeString(bstr);
            bstr = 0;
        }
        pStatus->Release();
    }

    // clean up.
    pStatus->Release();
```

