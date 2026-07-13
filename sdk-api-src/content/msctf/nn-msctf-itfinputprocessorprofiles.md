---
UID: NN:msctf.ITfInputProcessorProfiles
title: ITfInputProcessorProfiles (msctf.h)
description: The ITfInputProcessorProfiles interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.
helpviewer_keywords: ["ITfInputProcessorProfiles","ITfInputProcessorProfiles interface [Text Services Framework]","ITfInputProcessorProfiles interface [Text Services Framework]","described","_tsf_itfinputprocessorprofiles_ref","msctf/ITfInputProcessorProfiles","tsf.itfinputprocessorprofiles"]
old-location: tsf\itfinputprocessorprofiles.htm
tech.root: TSF
ms.assetid: 9fa722a4-1e3f-4845-aea7-3b24b517f2a5
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles, ITfInputProcessorProfiles interface [Text Services Framework], ITfInputProcessorProfiles interface [Text Services Framework],described, _tsf_itfinputprocessorprofiles_ref, msctf/ITfInputProcessorProfiles, tsf.itfinputprocessorprofiles
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfiles
 - msctf/ITfInputProcessorProfiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfInputProcessorProfiles
---

# ITfInputProcessorProfiles interface


## -description

The <b>ITfInputProcessorProfiles</b> interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.

## -inheritance

The <b>ITfInputProcessorProfiles</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfiles</b> also has these types of members:

## -remarks

To obtain a pointer to this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_TF_InputProcessorProfiles.


#### Examples

<b>ITfInputProcessorProfiles</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfInputProcessorProfiles *pProfiles;

//Create the object. 
hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                        NULL, 
                        CLSCTX_INPROC_SERVER, 
                        IID_ITfInputProcessorProfiles, 
                        (LPVOID*)&pProfiles);

if(SUCCEEDED(hr))
{
    //Use the interface. 

    //Release the interface. 
    pProfiles->Release();
}

```
