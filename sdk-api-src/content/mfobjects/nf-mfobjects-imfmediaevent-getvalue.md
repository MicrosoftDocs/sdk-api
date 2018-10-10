---
UID: NF:mfobjects.IMFMediaEvent.GetValue
title: IMFMediaEvent::GetValue
author: windows-sdk-content
description: Retrieves the value associated with the event, if any. The value is retrieved as a PROPVARIANT structure. The actual data type and the meaning of the value depend on the event.
old-location: mf\imfmediaevent_getvalue.htm
tech.root: medfound
ms.assetid: 05e57b40-2565-4312-866e-50f0c7d62c4a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 05e57b40-2565-4312-866e-50f0c7d62c4a, GetValue, GetValue method [Media Foundation], GetValue method [Media Foundation],IMFMediaEvent interface, IMFMediaEvent interface [Media Foundation],GetValue method, IMFMediaEvent.GetValue, IMFMediaEvent::GetValue, mf.imfmediaevent_getvalue, mfobjects/IMFMediaEvent::GetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaEvent.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEvent::GetValue


## -description



Retrieves the value associated with the event, if any. The value is retrieved as a <b>PROPVARIANT</b> structure. The actual data type and the meaning of the value depend on the event.




## -parameters




### -param pvValue [out]

Pointer to a <b>PROPVARIANT</b> structure. The method fills this structure with the data.


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
</table>
 




## -remarks



Before calling this method, call <b>PropVariantInit</b> to initialize the <b>PROPVARIANT</b> structure. After the method returns, call <b>PropVariantClear</b> to free the memory that was allocated for the <b>PROPVARIANT</b> data.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following function gets the event value if the value is an <b>IUnknown</b> pointer. If the <b>PROPVARIANT</b> type is not <b>VT_UNKOWN</b>, the function returns <b>MF_E_INVALIDTYPE</b>.


```cpp
//  Gets an IUnknown pointer from an IMFMediaEvent event and queries 
//  the pointer for a specified interface.
//
//  NOTE: Applies only to events that contain IUnknown pointers.
//        Otherwise, the function returns MF_E_INVALIDTYPE.

template <class Q>
HRESULT GetEventObject(IMFMediaEvent *pEvent, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    PROPVARIANT var;
    HRESULT hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt == VT_UNKNOWN)
        {
            hr = var.punkVal->QueryInterface(ppObject);
        }
        else
        {
            hr = MF_E_INVALIDTYPE;
        }
        PropVariantClear(&var);
    }
    return hr;
}


```





## -see-also




<a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a>



<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>
 

 

