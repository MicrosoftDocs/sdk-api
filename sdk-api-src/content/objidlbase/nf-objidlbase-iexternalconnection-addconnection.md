---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IExternalConnection::AddConnection


## -description


Increments the count of an object's strong external connections.


## -parameters




### -param extconn [in]

The type of external connection to the object. The only type of external connection currently supported by this interface is strong, which means that the object must remain alive as long as this external connection exists. Strong external connections are represented by the value EXTCONN_STRONG, which is defined in the enumeration <a href="https://msdn.microsoft.com/95c7de47-9f81-4316-99b8-0f5f0aa54d65">EXTCONN</a>.


### -param reserved [in]

Information about the connection. This parameter is reserved for use by OLE. Its value can be zero, but not necessarily. Therefore, implementations of <b>AddConnection</b> should not contain blocks of code whose execution depends on whether a zero value is returned.


## -returns



The method returns the count of connections. This value is intended to be used only for debugging purposes.




## -remarks



An object created by a EXE object server relies on its stub manager to call <b>AddConnection</b> whenever a link client activates and therefore creates an external lock on the object. When the link client breaks the connection, the stub manager calls <a href="https://msdn.microsoft.com/7ed598b2-9603-454a-99cf-849715e43ca1">IExternalConnection::ReleaseConnection</a> to release the lock.

DLL object applications exist in the same process space as their objects, so they do not use RPC (remote procedure calls) and do not have stub managers to keep track of external connections. Therefore, DLL servers that support external links to their objects must implement <a href="https://msdn.microsoft.com/28afc305-d5b0-4ac9-9412-5876e575c2c2">IExternalConnection</a> so that link clients can directly call the interface to inform them when connections are added or released.

The following is a typical implementation for the <b>AddConnection</b> method.

<pre class="syntax" xml:space="preserve"><code>DWORD MyInterface::AddConnection(DWORD extconn, DWORD dwReserved)
{
    return extconn &amp; EXTCONN_STRONG ? ++m_cStrong : 0;
}
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/28afc305-d5b0-4ac9-9412-5876e575c2c2">IExternalConnection</a>



<a href="https://msdn.microsoft.com/ce501785-16ad-4120-abea-41e2d6ca67df">IRunnableObject::LockRunning</a>



<a href="https://msdn.microsoft.com/84941a59-6880-4824-b4b9-cd1b52d2bffb">OleLockRunning</a>
 

 

