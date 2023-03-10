---
UID: NF:wbemcli.IEnumWbemClassObject.Next
title: IEnumWbemClassObject::Next (wbemcli.h)
description: Use the IEnumWbemClassObject::Next method to get one or more objects starting at the current position in an enumeration.
helpviewer_keywords: ["IEnumWbemClassObject interface [Windows Management Instrumentation]","Next method","IEnumWbemClassObject.Next","IEnumWbemClassObject::Next","Next","Next method [Windows Management Instrumentation]","Next method [Windows Management Instrumentation]","IEnumWbemClassObject interface","_hmm_ienumwbemclassobject_next","wbemcli/IEnumWbemClassObject::Next","wmi.ienumwbemclassobject_next"]
old-location: wmi\ienumwbemclassobject_next.htm
tech.root: wmi
ms.assetid: 8bde633b-b04a-4a21-82ce-f5aab1d32d95
ms.date: 12/05/2018
ms.keywords: IEnumWbemClassObject interface [Windows Management Instrumentation],Next method, IEnumWbemClassObject.Next, IEnumWbemClassObject::Next, Next, Next method [Windows Management Instrumentation], Next method [Windows Management Instrumentation],IEnumWbemClassObject interface, _hmm_ienumwbemclassobject_next, wbemcli/IEnumWbemClassObject::Next, wmi.ienumwbemclassobject_next
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
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWbemClassObject::Next
 - wbemcli/IEnumWbemClassObject::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IEnumWbemClassObject.Next
---

# IEnumWbemClassObject::Next


## -description

Use the <b>IEnumWbemClassObject::Next</b> method to 
    get one or more objects starting at the current position in an enumeration. This method advances the current 
    position in the enumeration by <i>uCount</i> objects, so that subsequent calls return the 
    subsequent objects.

## -parameters

### -param lTimeout [in]

Specifies the maximum amount of time in milliseconds that the call blocks before returning. If you use the 
      constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until objects are available. If 
      you use the value 0 (<b>WBEM_NO_WAIT</b>), the call returns immediately, whether any objects 
      are available or not.

### -param uCount [in]

Number of requested objects.

### -param apObjects [out]

Pointer to enough storage to hold the number of 
      <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface pointers specified by 
      <i>uCount</i>. This storage must be supplied by the caller. This parameter cannot be 
      <b>NULL</b>. The caller must call <b>Release</b> on each of the received 
      interface pointers when they are no longer needed.

### -param puReturned [out]

Pointer to a <b>ULONG</b> that receives the number of objects returned. This number can 
       be less than the number requested in <i>uCount</i>. This pointer cannot be 
       <b>NULL</b>.

<div class="alert"><b>Note</b>  The <b>Next</b> method returns 
       <b>WBEM_S_FALSE</b> when you have reached the end of the enumeration, even if objects have 
       been returned successfully. The <b>WBEM_S_NO_ERROR</b> value returns only when the number of 
       objects returned matches the number requested in <i>uCount</i>. The 
       <b>WBEM_S_TIMEDOUT</b> value is returned when the number of objects returned is less than 
       the number requested but you are not at the end of the enumeration. Therefore, you should use loop termination 
       logic that examines the <i>puReturned</i> value to ensure that you have reached the end of 
       the enumeration.</div>
<div> </div>

## -returns

The <b>Next</b> method returns an <b>HRESULT</b> indicating 
      the status of the method call. The following list lists the value contained within an 
      <b>HRESULT</b>.

## -remarks

You may see COM-specific error codes returned if network problems cause you to lose the remote connection to Windows Management. On error, you can call the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a> to obtain more error information.

If more than one object is requested, and if the number of requested objects is returned, the function returns <b>WBEM_S_NO_ERROR</b>. If less than the requested number of objects is available, and if the enumeration has completed, those objects are returned and the function returns <b>WBEM_S_FALSE</b>.

If the enumeration has not completed, the call waits for objects to be available up to the specified time-out. If the enumeration times out before the objects are available, the function returns <b>WBEM_S_TIMEDOUT</b>.

<div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.</div>
<div> </div>

#### Examples

For an extended discussion and example of making queries in C++ and WMI, see Making <a href="https://www.codeproject.com/Articles/10539/Making-WMI-Queries-In-C">WMI Queries In C++</a> on CodeProject.

<div class="code"></div>
In the following code, more than one object is requested:


```cpp
HRESULT ProcessEnum( IEnumWbemClassObject*    pEnum )
{
    HRESULT    hRes = WBEM_S_NO_ERROR;

    // Final Next will return WBEM_S_FALSE
    while ( WBEM_S_NO_ERROR == hRes )
    {
        ULONG            uReturned;
        IWbemClassObject*    apObj[10];

        hRes = pEnum->Next( WBEM_INFINITE, 10, apObj, &uReturned );

        if ( SUCCEEDED( hRes ) )
        {
            // Do something with the objects.
            //ProcessObjects( uReturned,  apObj );

            for ( ULONG n = 0; n < uReturned; n++ )
            {
                apObj[n]->Release();
            }

        }    // If Enum succeeded...
    }    // While Enum is returning objects...

    return hRes;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/enumerating-wmi">Enumerating WMI</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject">IEnumWbemClassObject</a>