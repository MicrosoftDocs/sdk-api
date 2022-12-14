---
UID: NN:functiondiscoveryapi.IFunctionDiscoveryNotification
title: IFunctionDiscoveryNotification (functiondiscoveryapi.h)
description: This interface is implemented by the client program to support asynchronous queries and is called by Function Discovery to notify the client program when a function instance that meets the query parameters has been added or removed.
helpviewer_keywords: ["IFunctionDiscoveryNotification","IFunctionDiscoveryNotification interface","IFunctionDiscoveryNotification interface","described","functiondiscoveryapi/IFunctionDiscoveryNotification","ncd.ifunctiondiscoverynotification"]
old-location: ncd\ifunctiondiscoverynotification.htm
tech.root: ncd
ms.assetid: 1819fe08-b151-482d-8e2c-1d599fd15609
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryNotification, IFunctionDiscoveryNotification interface, IFunctionDiscoveryNotification interface,described, functiondiscoveryapi/IFunctionDiscoveryNotification, ncd.ifunctiondiscoverynotification
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
 - IFunctionDiscoveryNotification
 - functiondiscoveryapi/IFunctionDiscoveryNotification
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
 - IFunctionDiscoveryNotification
---

# IFunctionDiscoveryNotification interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is implemented by the client program  to support asynchronous queries and is called by Function Discovery to notify the client program when a function instance that meets the query parameters has been added or removed.

## -inheritance

The <b>IFunctionDiscoveryNotification</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryNotification</b> also has these types of members:

## -remarks

This interface must be implemented by the client program in order to receive notifications from Function Discovery. The address of the client program's implementation is passed to one of the query methods to enable notifications for function instances which meet the query parameters.

 Function Discovery calls the client program's <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onupdate">IFunctionDiscoveryNotification::OnUpdate</a> method to perform the actual notification, which is generated for a function instance when it is added or removed. <div class="alert"><b>Note</b>  Some Function discovery providers will also generate a notification when a function instance is modified by changing a category or one or more properties assigned to it.</div>
<div> </div>



#### Examples

The examples that appear on individual method pages are based on the following class declaration.


``` syntax
class CMyNotificationListener : public CFunctionDiscoveryNotificationWrapper
{
public:
    CMyNotificationListener() {
        m_hAddEvent      = CreateEvent( NULL, FALSE, FALSE, NULL );
        m_hRemoveEvent   = CreateEvent( NULL, FALSE, FALSE, NULL );
        m_hChangeEvent   = CreateEvent( NULL, FALSE, FALSE, NULL );
    }

    ~CMyNotificationListener() {
        CloseHandle( m_hAddEvent );
        CloseHandle( m_hRemoveEvent );
        CloseHandle( m_hChangeEvent );
    }
        

private:
    HANDLE m_hAddEvent, m_hRemoveEvent, m_hChangeEvent;
};

```

