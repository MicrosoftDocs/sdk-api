---
UID: NF:objidlbase.IExternalConnection.ReleaseConnection
title: IExternalConnection::ReleaseConnection (objidlbase.h)
description: The IExternalConnection::ReleaseConnection (objidlbase.h) method decrements the count of an object's strong external connections.
helpviewer_keywords: ["IExternalConnection interface [COM]","ReleaseConnection method","IExternalConnection.ReleaseConnection","IExternalConnection::ReleaseConnection","ReleaseConnection","ReleaseConnection method [COM]","ReleaseConnection method [COM]","IExternalConnection interface","_com_iexternalconnection_releaseconnection","com.iexternalconnection_releaseconnection","objidlbase/IExternalConnection::ReleaseConnection"]
old-location: com\iexternalconnection_releaseconnection.htm
tech.root: com
ms.assetid: 7ed598b2-9603-454a-99cf-849715e43ca1
ms.date: 08/13/2022
ms.keywords: IExternalConnection interface [COM],ReleaseConnection method, IExternalConnection.ReleaseConnection, IExternalConnection::ReleaseConnection, ReleaseConnection, ReleaseConnection method [COM], ReleaseConnection method [COM],IExternalConnection interface, _com_iexternalconnection_releaseconnection, com.iexternalconnection_releaseconnection, objidlbase/IExternalConnection::ReleaseConnection
req.header: objidlbase.h
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
 - IExternalConnection::ReleaseConnection
 - objidlbase/IExternalConnection::ReleaseConnection
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
 - IExternalConnection.ReleaseConnection
---

# IExternalConnection::ReleaseConnection


## -description

Decrements the count of an object's strong external connections.

## -parameters

### -param extconn [in]

The type of external connection to the object. The only type of external connection currently supported by this interface is strong, which means that the object must remain alive as long as this external connection exists. Strong external connections are represented by the value EXTCONN_STRONG, which is defined in the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-extconn">EXTCONN</a>.

### -param reserved [in]

Information about the connection. This parameter is reserved for use by OLE. Its value can be zero, but not necessarily. Therefore, implementations of <b>ReleaseConnection</b> should not contain blocks of code whose execution depends on whether a zero value is returned.

### -param fLastReleaseCloses [in]

This parameter is <b>TRUE</b> if the connection being released is the last external lock on the object, and therefore the object should close. Otherwise, the object should remain open until closed by the user or another process.

## -returns

The method returns the count of connections. This value is intended to be used only for debugging purposes.

## -remarks

If <i>fLastReleaseCloses</i> equals <b>TRUE</b>, calling <b>ReleaseConnection</b> causes the object to shut itself down. Calling this method is the only way in which a DLL object, running in the same process space as the container application, will know when to close following a silent update.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iexternalconnection">IExternalConnection</a>
