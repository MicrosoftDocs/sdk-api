---
UID: NF:imapi2.IDiscMaster2.get_Item
title: IDiscMaster2::get_Item (imapi2.h)
description: Retrieves the unique identifier of the specified disc device.
helpviewer_keywords: ["IDiscMaster2 interface [IMAPI]","get_Item method","IDiscMaster2.get_Item","IDiscMaster2::get_Item","get_Item","get_Item method [IMAPI]","get_Item method [IMAPI]","IDiscMaster2 interface","imapi.idiscmaster2_get_item","imapi2/IDiscMaster2::get_Item"]
old-location: imapi\idiscmaster2_get_item.htm
tech.root: imapi
ms.assetid: e909acb9-850b-404d-a2f7-efb37faf3506
ms.date: 12/05/2018
ms.keywords: IDiscMaster2 interface [IMAPI],get_Item method, IDiscMaster2.get_Item, IDiscMaster2::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IDiscMaster2 interface, imapi.idiscmaster2_get_item, imapi2/IDiscMaster2::get_Item
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMaster2::get_Item
 - imapi2/IDiscMaster2::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscMaster2.get_Item
---

# IDiscMaster2::get_Item


## -description

Retrieves the unique identifier of the specified disc device.

## -parameters

### -param index [in]

Zero-based index of the device whose unique identifier you want to retrieve.

The index value can change during PNP activity when devices are added or removed from the computer,  or across boot sessions.

### -param value [out]

String that contains the unique identifier of the disc device associated with the specified index.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

To enumerate all identifiers, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get__newenum">IDiscMaster2::get__NewEnum</a> method.

The following sample demonstrates how to re-enumerate optical drives in order to accurately account for drives added or removed  after the initial creation of the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a> object. This is accomplished via the <b>IDiscMaster2::get_Item</b> and <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_count">IDiscMaster2::get_Count</a> methods:


```cpp
#include <windows.h>
#include <tchar.h>
#include <imapi2.h>
#include <objbase.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "user32.lib")

int __cdecl _tmain(int argc, TCHAR* argv[])   
{   
    BSTR           bstrDeviceName;   
    HRESULT        hr = S_OK;   
    BOOL           bComInitialised;       
    IDiscMaster2*  discMaster;   
    UINT           iCounter = 0; 
    LONG           lValue = 0; 

    bComInitialised = SUCCEEDED(CoInitializeEx(0, COINIT_MULTITHREADED));

    // Create an object of IDiscMaster2  
    if (SUCCEEDED(hr)){
        CoCreateInstance(
            CLSID_MsftDiscMaster2,
            NULL, CLSCTX_ALL,
            IID_PPV_ARGS(&discMaster)
        );   

        if(FAILED(hr)){
            _tprintf(TEXT("\nUnsuccessful in creating an instance of CLSID_MsftDiscMaster2.\n\nError returned: 0x%x\n"), hr);
            return 0;
        }
    }
    //
    // Loop twice and get the optical drives attached to the system,
    // first time just get the current configuration and second time 
    // prompt the user to change the configuration and then get the 
    // altered configuration.   
    //
    do{
        // Get the number of drives 
        if (SUCCEEDED(hr)){
            hr = discMaster->get_Count(&lValue);
            if (SUCCEEDED(hr)){
                _tprintf(TEXT("\nTotal number of drives = %d\n"), lValue);
            }
        }

        // Print all the optical drives attached to the system 
        if (SUCCEEDED(hr)){
            for(LONG iCount = 0; iCount < lValue; iCount++) {
                hr = discMaster->get_Item(iCount, &bstrDeviceName);
                _tprintf(TEXT("\nUnique identifier of the disc device associated with index %d is: %s\n"), iCount, bstrDeviceName);
            }            
        }

        // Prompt the user to unhook or add drives
        if (iCounter < 1){
            MessageBox(NULL,TEXT("Please un-hook or add drives and hit OK"), TEXT("Manual Action"), MB_OK);
            _tprintf(TEXT("\nGetting the altered configuration ... \n"));
        }
        iCounter++;
    }while(iCounter < 2);

    discMaster->Release();
    CoUninitialize();   
    bComInitialised = FALSE;   

    return 0;

```

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_count">IDiscMaster2::get_Count</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-initializediscrecorder">IDiscRecorder2::InitializeDiscRecorder</a>