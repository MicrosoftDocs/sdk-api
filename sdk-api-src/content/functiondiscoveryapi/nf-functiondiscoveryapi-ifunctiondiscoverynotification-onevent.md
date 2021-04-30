---
UID: NF:functiondiscoveryapi.IFunctionDiscoveryNotification.OnEvent
title: IFunctionDiscoveryNotification::OnEvent (functiondiscoveryapi.h)
description: Receives any add, remove, or update events during a notification.
helpviewer_keywords: ["FD_EVENTID_ASYNCTHREADEXIT","FD_EVENTID_IPADDRESSCHANGE","FD_EVENTID_SEARCHCOMPLETE","FD_EVENTID_SEARCHSTART","IFunctionDiscoveryNotification interface","OnEvent method","IFunctionDiscoveryNotification.OnEvent","IFunctionDiscoveryNotification::OnEvent","OnEvent","OnEvent method","OnEvent method","IFunctionDiscoveryNotification interface","functiondiscoveryapi/IFunctionDiscoveryNotification::OnEvent","ncd.ifunctiondiscoverynotification_onevent"]
old-location: ncd\ifunctiondiscoverynotification_onevent.htm
tech.root: ncd
ms.assetid: 4ebfdf15-ca37-4905-b842-8854a0bd276b
ms.date: 12/05/2018
ms.keywords: FD_EVENTID_ASYNCTHREADEXIT, FD_EVENTID_IPADDRESSCHANGE, FD_EVENTID_SEARCHCOMPLETE, FD_EVENTID_SEARCHSTART, IFunctionDiscoveryNotification interface,OnEvent method, IFunctionDiscoveryNotification.OnEvent, IFunctionDiscoveryNotification::OnEvent, OnEvent, OnEvent method, OnEvent method,IFunctionDiscoveryNotification interface, functiondiscoveryapi/IFunctionDiscoveryNotification::OnEvent, ncd.ifunctiondiscoverynotification_onevent
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
 - IFunctionDiscoveryNotification::OnEvent
 - functiondiscoveryapi/IFunctionDiscoveryNotification::OnEvent
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
 - IFunctionDiscoveryNotification.OnEvent
---

# IFunctionDiscoveryNotification::OnEvent


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Receives any add, remove, or update events during a notification.

## -parameters

### -param dwEventID [in]

The type of event.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FD_EVENTID_SEARCHCOMPLETE"></a><a id="fd_eventid_searchcomplete"></a><dl>
<dt><b>FD_EVENTID_SEARCHCOMPLETE</b></dt>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
The search was completed by a provider. Typically, this notification is sent by network protocol providers where the protocol specifies a defined interval in which search results will be accepted.  Both the WSD and <a href="/previous-versions/windows/desktop/fundisc/ssdp-provider">SSDP</a> providers use this event type. 

Once this notification is sent, a query ignores all incoming responses to the initial search or probe request. However, the query will still monitor for Hello or Bye messages (used to indicate when a device is added or removed). The query will continue to monitor for these events until <b>Release</b> is called on the query object.

This notification will not be sent if a catastrophic error occurs.

For information about how this event is implemented or used by a specific provider, follow the link to the provider documentation from the  <a href="/previous-versions/windows/desktop/fundisc/built-in-providers">Built-in Providers</a> topic.

</td>
</tr>
<tr>
<td width="40%"><a id="FD_EVENTID_ASYNCTHREADEXIT"></a><a id="fd_eventid_asyncthreadexit"></a><dl>
<dt><b>FD_EVENTID_ASYNCTHREADEXIT</b></dt>
<dt>1001</dt>
</dl>
</td>
<td width="60%">
Not used by Function Discovery clients.

</td>
</tr>
<tr>
<td width="40%"><a id="FD_EVENTID_SEARCHSTART"></a><a id="fd_eventid_searchstart"></a><dl>
<dt><b>FD_EVENTID_SEARCHSTART</b></dt>
<dt>1002</dt>
</dl>
</td>
<td width="60%">
Not used by Function Discovery clients.

</td>
</tr>
<tr>
<td width="40%"><a id="FD_EVENTID_IPADDRESSCHANGE"></a><a id="fd_eventid_ipaddresschange"></a><dl>
<dt><b>FD_EVENTID_IPADDRESSCHANGE</b></dt>
<dt>1003</dt>
</dl>
</td>
<td width="60%">
The IP address of the NIC changed. The WSD provider implements this notification. Events may be sent when a power event occurs (for example, when machine wakes from sleep) or when roaming with a laptop.

<div class="alert"><b>Note</b>  This value is not available for use on Windows Vista. It is available on Windows Vista with SP1, Windows Server 2008, and subsequent versions of the operating system.</div>
<div> </div>
</td>
</tr>
</table>

### -param fdqcQueryContext [in]

The context registered for change notification. The type <b>FDQUERYCONTEXT</b> is defined as a <b>DWORDLONG</b>. This parameter can be <b>NULL</b>.

### -param pszProvider [in]

The name of the provider.

## -returns

The client program's implementation of the <b>OnEvent</b> method should return one of the following <b>HRESULT</b> values to the caller.

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

Function Discovery providers (SSDP and WSD) use this method to implement notifications that a search pass is complete.

Do not call <b>Release</b> on the query object from this method. Doing so could cause a deadlock. If <b>Release</b>  is called on a query object from another thread while a callback is in process, the object will not be released until the callback has finished.

All notifications passed to Function Discovery by providers are queued and returned to the client one by one. Callbacks are synchronized so that a client will only receive one notification at a time.

Because other <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> method calls may be made in other threads, any changes made to the thread state during the call  must be restored before exiting the method.


#### Examples

The following example shows an OnEvent handler implementation. The <b>CMyNotificationListener</b> class is defined in the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> topic.


```cpp
#include <windows.h>

HRESULT CMyNotificationListener::OnEvent(
                                         IN DWORD dwEventID,
                                         IN FDQUERYCONTEXT fdqcQueryContext,
                                         IN const WCHAR * pszProvider
                                         )
{
    HRESULT hr = S_OK;
    HANDLE hSearchComplete = INVALID_HANDLE_VALUE;
    hSearchComplete = OpenEventW( EVENT_ALL_ACCESS, 
                                  FALSE, 
                                  L"SearchComplete" );
    
    if( NULL == hSearchComplete )
    {
        return hr;
    }

    if( FD_EVENTID_SEARCHCOMPLETE == dwEventID )
    {
        SetEvent( hSearchComplete );
    }

    CloseHandle( hSearchComplete );
    
    return hr;
} 

```

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a>