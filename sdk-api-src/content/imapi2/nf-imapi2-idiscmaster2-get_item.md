---
UID: NF:imapi2.IDiscMaster2.get_Item
title: IDiscMaster2::get_Item
author: windows-sdk-content
description: Retrieves the unique identifier of the specified disc device.
old-location: imapi\idiscmaster2_get_item.htm
old-project: imapi
ms.assetid: e909acb9-850b-404d-a2f7-efb37faf3506
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDiscMaster2 interface [IMAPI],get_Item method, IDiscMaster2.get_Item, IDiscMaster2::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IDiscMaster2 interface, imapi.idiscmaster2_get_item, imapi2/IDiscMaster2::get_Item
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscMaster2.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



To enumerate all identifiers, call the <a href="https://msdn.microsoft.com/f148a1c0-cb76-40e9-9749-a074f04c93e8">IDiscMaster2::get__NewEnum</a> method.

    The following sample demonstrates how to re-enumerate optical 
    drives in order to accurately account for drives added or removed  after the initial creation of the <a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a> object. This is accomplished via the <b>IDiscMaster2::get_Item</b> and <a href="https://msdn.microsoft.com/b1e0ec8f-4c66-4648-ad76-2998200ea574">IDiscMaster2::get_Count</a> methods:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;tchar.h&gt;
#include &lt;imapi2.h&gt;
#include &lt;objbase.h&gt;
#include &lt;stdio.h&gt;

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
            IID_PPV_ARGS(&amp;discMaster)
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
            hr = discMaster-&gt;get_Count(&amp;lValue);
            if (SUCCEEDED(hr)){
                _tprintf(TEXT("\nTotal number of drives = %d\n"), lValue);
            }
        }

        // Print all the optical drives attached to the system 
        if (SUCCEEDED(hr)){
            for(LONG iCount = 0; iCount &lt; lValue; iCount++) {
                hr = discMaster-&gt;get_Item(iCount, &amp;bstrDeviceName);
                _tprintf(TEXT("\nUnique identifier of the disc device associated with index %d is: %s\n"), iCount, bstrDeviceName);
            }            
        }

        // Prompt the user to unhook or add drives
        if (iCounter &lt; 1){
            MessageBox(NULL,TEXT("Please un-hook or add drives and hit OK"), TEXT("Manual Action"), MB_OK);
            _tprintf(TEXT("\nGetting the altered configuration ... \n"));
        }
        iCounter++;
    }while(iCounter &lt; 2);

    discMaster-&gt;Release();
    CoUninitialize();   
    bComInitialised = FALSE;   

    return 0;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>



<a href="https://msdn.microsoft.com/b1e0ec8f-4c66-4648-ad76-2998200ea574">IDiscMaster2::get_Count</a>



<a href="https://msdn.microsoft.com/19a647b3-ef39-4208-9dfc-e52242a88c6c">IDiscRecorder2::InitializeDiscRecorder</a>
 

 

