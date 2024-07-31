---
UID: NF:objidl.IExternalConnection.AddConnection
title: IExternalConnection::AddConnection (objidl.h)
description: The IExternalConnection::AddConnection method (objidl.h) increments the count of an object's strong external connections.
helpviewer_keywords: ["AddConnection","AddConnection method [COM]","AddConnection method [COM]","IExternalConnection interface","IExternalConnection interface [COM]","AddConnection method","IExternalConnection.AddConnection","IExternalConnection::AddConnection","_com_iexternalconnection_addconnection","com.iexternalconnection_addconnection","objidlbase/IExternalConnection::AddConnection"]
old-location: com\iexternalconnection_addconnection.htm
tech.root: com
ms.assetid: 7439cb16-1da3-4fab-a16d-519f9ce1053a
ms.date: 08/12/2022
ms.keywords: AddConnection, AddConnection method [COM], AddConnection method [COM],IExternalConnection interface, IExternalConnection interface [COM],AddConnection method, IExternalConnection.AddConnection, IExternalConnection::AddConnection, _com_iexternalconnection_addconnection, com.iexternalconnection_addconnection, objidlbase/IExternalConnection::AddConnection
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IExternalConnection::AddConnection
 - objidl/IExternalConnection::AddConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IExternalConnection.AddConnection
---

# IExternalConnection::AddConnection


## -description

Increments the count of an object's strong external connections.

## -parameters

### -param extconn [in]

The type of external connection to the object. The only type of external connection currently supported by this interface is strong, which means that the object must remain alive as long as this external connection exists. Strong external connections are represented by the value EXTCONN_STRONG, which is defined in the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-extconn">EXTCONN</a>.

### -param reserved [in]

Information about the connection. This parameter is reserved for use by OLE. Its value can be zero, but not necessarily. Therefore, implementations of <b>AddConnection</b> should not contain blocks of code whose execution depends on whether a zero value is returned.

## -returns

The method returns the count of connections. This value is intended to be used only for debugging purposes.

## -remarks

An object created by a EXE object server relies on its stub manager to call <b>AddConnection</b> whenever a link client activates and therefore creates an external lock on the object. When the link client breaks the connection, the stub manager calls <a href="/windows/desktop/api/objidl/nf-objidl-iexternalconnection-releaseconnection">IExternalConnection::ReleaseConnection</a> to release the lock.

DLL object applications exist in the same process space as their objects, so they do not use RPC (remote procedure calls) and do not have stub managers to keep track of external connections. Therefore, DLL servers that support external links to their objects must implement <a href="/windows/desktop/api/objidl/nn-objidl-iexternalconnection">IExternalConnection</a> so that link clients can directly call the interface to inform them when connections are added or released.

The following is a typical implementation for the <b>AddConnection</b> method.


``` syntax
DWORD MyInterface::AddConnection(DWORD extconn, DWORD dwReserved)
{
    return extconn & EXTCONN_STRONG ? ++m_cStrong : 0;
}

```


## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iexternalconnection">IExternalConnection</a>



<a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-lockrunning">IRunnableObject::LockRunning</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olelockrunning">OleLockRunning</a>
