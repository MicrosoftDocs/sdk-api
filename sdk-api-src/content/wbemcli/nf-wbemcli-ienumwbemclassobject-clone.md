---
UID: NF:wbemcli.IEnumWbemClassObject.Clone
title: IEnumWbemClassObject::Clone (wbemcli.h)
description: The IEnumWbemClassObject::Clone method makes a logical copy of the entire enumerator, retaining its current position in an enumeration.
helpviewer_keywords: ["Clone","Clone method [Windows Management Instrumentation]","Clone method [Windows Management Instrumentation]","IEnumWbemClassObject interface","IEnumWbemClassObject interface [Windows Management Instrumentation]","Clone method","IEnumWbemClassObject.Clone","IEnumWbemClassObject::Clone","_hmm_ienumwbemclassobject_clone","wbemcli/IEnumWbemClassObject::Clone","wmi.ienumwbemclassobject_clone"]
old-location: wmi\ienumwbemclassobject_clone.htm
tech.root: wmi
ms.assetid: a323c662-e005-44aa-a903-1eb7d6ddff9e
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Management Instrumentation], Clone method [Windows Management Instrumentation],IEnumWbemClassObject interface, IEnumWbemClassObject interface [Windows Management Instrumentation],Clone method, IEnumWbemClassObject.Clone, IEnumWbemClassObject::Clone, _hmm_ienumwbemclassobject_clone, wbemcli/IEnumWbemClassObject::Clone, wmi.ienumwbemclassobject_clone
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
 - IEnumWbemClassObject::Clone
 - wbemcli/IEnumWbemClassObject::Clone
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
 - IEnumWbemClassObject.Clone
---

# IEnumWbemClassObject::Clone


## -description

The <b>IEnumWbemClassObject::Clone</b> method makes 
    a logical copy of the entire enumerator, retaining its current position in an enumeration. This method makes only 
    a "best effort" copy. Due to the dynamic nature of many CIM objects, it is possible that the new enumerator does 
    not enumerate the same set of objects as the source enumerator.
<div class="alert"><b>Note</b>  <p class="note">When the enumeration is initialized with the <b>WBEM_FLAG_FORWARD_ONLY</b> flag, 
     <b>IEnumWbemClassObject::Clone</b> is not 
     supported.

<p class="note">Any pending asynchronous deliveries begun by 
     <a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync">NextAsync</a> are not cloned.

</div><div> </div>

## -parameters

### -param ppEnum [out]

Receives a pointer to a new 
      <a href="/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject">IEnumWbemClassObject</a> object. The caller must call 
      <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the interface pointer is no longer 
      required. On error, there will not be a return of a new object.

## -returns

On error, you can call the COM function 
       <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a> to obtain more error 
       information. COM-specific error codes may also be returned if network problems cause you to lose the remote 
       connection to Windows Management.

The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

Because the call-back to the sink might not be returned at the same authentication level as the client 
    requires, it is recommended that you use semisynchronous communication instead of asynchronous. If you require 
    asynchronous communication, see 
    <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see 
    <a href="/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject">IEnumWbemClassObject</a> and 
    <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.


#### Examples

The following code shows how to use the <b>IEnumWbemClassObject::Clone</b> method.


```cpp
BOOL CloneEnum(IEnumWbemClassObject *pSrc)
{
    IEnumWbemClassObject *pCopy = 0;

    HRESULT hRes = pSrc->Clone(&pCopy);

    if (hRes != WBEM_S_NO_ERROR)       // Failed to clone it.
        return FALSE;

    // Use the copy of the enumerator.
    // ...

    pCopy->Release();

    return TRUE;
}
```