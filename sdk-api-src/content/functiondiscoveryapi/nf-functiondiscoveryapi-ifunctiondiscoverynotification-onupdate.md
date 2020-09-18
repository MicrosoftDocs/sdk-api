---
UID: NF:functiondiscoveryapi.IFunctionDiscoveryNotification.OnUpdate
title: IFunctionDiscoveryNotification::OnUpdate (functiondiscoveryapi.h)
description: Indicates that a function instance has been added, removed, or changed.
helpviewer_keywords: ["IFunctionDiscoveryNotification interface","OnUpdate method","IFunctionDiscoveryNotification.OnUpdate","IFunctionDiscoveryNotification::OnUpdate","OnUpdate","OnUpdate method","OnUpdate method","IFunctionDiscoveryNotification interface","functiondiscoveryapi/IFunctionDiscoveryNotification::OnUpdate","ncd.ifunctiondiscoverynotification_onupdate_method"]
old-location: ncd\ifunctiondiscoverynotification_onupdate_method.htm
tech.root: ncd
ms.assetid: ab4d0fc6-de3f-49cf-b53c-573222a8bc89
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryNotification interface,OnUpdate method, IFunctionDiscoveryNotification.OnUpdate, IFunctionDiscoveryNotification::OnUpdate, OnUpdate, OnUpdate method, OnUpdate method,IFunctionDiscoveryNotification interface, functiondiscoveryapi/IFunctionDiscoveryNotification::OnUpdate, ncd.ifunctiondiscoverynotification_onupdate_method
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
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
 - IFunctionDiscoveryNotification::OnUpdate
 - functiondiscoveryapi/IFunctionDiscoveryNotification::OnUpdate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - functiondiscoveryapi.h
api_name:
 - IFunctionDiscoveryNotification.OnUpdate
---

# IFunctionDiscoveryNotification::OnUpdate


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Indicates that a function instance has been added, removed, or changed. This method is implemented by the client program and is called by Function Discovery.

## -parameters

### -param enumQueryUpdateAction [in]

A <a href="/windows/win32/api/functiondiscoveryapi/ne-functiondiscoveryapi-queryupdateaction">QueryUpdateAction</a> value that specifies the type of action Function Discovery is performing on the specified function instance.

### -param fdqcQueryContext [in]

The context registered for change notification. The type <b>FDQUERYCONTEXT</b> is defined as a DWORDLONG. This parameter can be <b>NULL</b>.

### -param pIFunctionInstance [in]

An <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface pointer that represents the function instance being affected by the update.

## -returns

The client program's implementation of the <b>OnUpdate</b> method should return one of the following <b>HRESULT</b> values to the caller.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of one of the input parameters is invalid.

</td>
</tr>
</table>

## -remarks

Do not call <b>Release</b> on the query object from this method. Doing so could cause a deadlock. If <b>Release</b>  is called on a query object from another thread while a callback is in process, the object will not be released until the callback has finished.

All notifications passed to Function Discovery by providers are queued and returned to the client one by one. Callbacks are synchronized so that a client will only receive one notification at a time.

Because other <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> method calls may be made in other threads, any changes made to the thread state during the call  must be restored before exiting the method.


#### Examples

The following code shows an OnUpdate handler implementation. The <b>CMyNotificationListener</b> class is defined in the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> topic.


```cpp
#include <windows.h>

HRESULT STDMETHODCALLTYPE CMyNotificationListener::OnUpdate(
                                          IN QueryUpdateAction Action,
                                          IN FDQUERYCONTEXT fdqcQueryContext,
                                          IN IFunctionInstance *pInstance)
{
    HRESULT hr = S_OK;

    switch (Action) {
    case QUA_ADD:
        SetEvent( m_hAddEvent );
        break;
    case QUA_REMOVE:
        SetEvent( m_hRemoveEvent );
        break;
    case QUA_CHANGE:
        SetEvent( m_hChangeEvent );
        break;
    }
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a>