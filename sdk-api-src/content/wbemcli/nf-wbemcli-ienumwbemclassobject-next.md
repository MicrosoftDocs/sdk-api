---
UID: NF:wbemcli.IEnumWbemClassObject.Next
title: IEnumWbemClassObject::Next method
author: windows-driver-content
description: Use the IEnumWbemClassObject::Next method to get one or more objects starting at the current position in an enumeration.
old-location: wmi\ienumwbemclassobject_next.htm
old-project: WmiSdk
ms.assetid: 8bde633b-b04a-4a21-82ce-f5aab1d32d95
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: IEnumWbemClassObject, IEnumWbemClassObject interface [Windows Management Instrumentation], Next method, IEnumWbemClassObject::Next, Next method [Windows Management Instrumentation], Next method [Windows Management Instrumentation], IEnumWbemClassObject interface, Next,IEnumWbemClassObject.Next, _hmm_ienumwbemclassobject_next, wbemcli/IEnumWbemClassObject::Next, wmi.ienumwbemclassobject_next
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
api_name:
-	IEnumWbemClassObject.Next
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWbemClassObject::Next method


## -description


Use the <b>IEnumWbemClassObject::Next</b> method to 
    get one or more objects starting at the current position in an enumeration. This method advances the current 
    position in the enumeration by <i>uCount</i> objects, so that subsequent calls return the 
    subsequent objects.


## -parameters




### -param lTimeout




### -param uCount [in]

Number of requested objects.


### -param apObjects




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

#### - lTimeOut [in]

Specifies the maximum amount of time in milliseconds that the call blocks before returning. If you use the 
      constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until objects are available. If 
      you use the value 0 (<b>WBEM_NO_WAIT</b>), the call returns immediately, whether any objects 
      are available or not.


#### - ppObjects [out]

Pointer to enough storage to hold the number of 
      <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface pointers specified by 
      <i>uCount</i>. This storage must be supplied by the caller. This parameter cannot be 
      <b>NULL</b>. The caller must call <b>Release</b> on each of the received 
      interface pointers when they are no longer needed.


## -returns



The <b>Next</b> method returns an <b>HRESULT</b> indicating 
      the status of the method call. The following list lists the value contained within an 
      <b>HRESULT</b>.




## -remarks



You may see COM-specific error codes returned if network problems cause you to lose the remote connection to Windows Management. On error, you can call the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a> to obtain more error information.

If more than one object is requested, and if the number of requested objects is returned, the function returns <b>WBEM_S_NO_ERROR</b>. If less than the requested number of objects is available, and if the enumeration has completed, those objects are returned and the function returns <b>WBEM_S_FALSE</b>.

If the enumeration has not completed, the call waits for objects to be available up to the specified time-out. If the enumeration times out before the objects are available, the function returns <b>WBEM_S_TIMEDOUT</b>.

<div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.</div>
<div> </div>

#### Examples

For an extended discussion and example of making queries in C++ and WMI, see Making <a href="http://www.codeproject.com/Articles/10539/Making-WMI-Queries-In-C">WMI Queries In C++</a> on CodeProject.

<div class="code"></div>
In the following code, more than one object is requested:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT ProcessEnum( IEnumWbemClassObject*    pEnum )
{
    HRESULT    hRes = WBEM_S_NO_ERROR;

    // Final Next will return WBEM_S_FALSE
    while ( WBEM_S_NO_ERROR == hRes )
    {
        ULONG            uReturned;
        IWbemClassObject*    apObj[10];

        hRes = pEnum-&gt;Next( WBEM_INFINITE, 10, apObj, &amp;uReturned );

        if ( SUCCEEDED( hRes ) )
        {
            // Do something with the objects.
            //ProcessObjects( uReturned,  apObj );

            for ( ULONG n = 0; n &lt; uReturned; n++ )
            {
                apObj[n]-&gt;Release();
            }

        }    // If Enum succeeded...
    }    // While Enum is returning objects...

    return hRes;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fe7e3259-9a7c-4f73-af30-192bbbace1b3">Enumerating WMI</a>



<a href="https://msdn.microsoft.com/142ea48d-d47b-4b7b-ab84-049a54955488">IEnumWbemClassObject</a>
 

 

