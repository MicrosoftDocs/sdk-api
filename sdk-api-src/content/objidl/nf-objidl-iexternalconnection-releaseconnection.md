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

# IExternalConnection::ReleaseConnection


## -description


Decrements the count of an object's strong external connections.


## -parameters




### -param extconn [in]

The type of external connection to the object. The only type of external connection currently supported by this interface is strong, which means that the object must remain alive as long as this external connection exists. Strong external connections are represented by the value EXTCONN_STRONG, which is defined in the enumeration <a href="https://msdn.microsoft.com/95c7de47-9f81-4316-99b8-0f5f0aa54d65">EXTCONN</a>.


### -param reserved [in]

Information about the connection. This parameter is reserved for use by OLE. Its value can be zero, but not necessarily. Therefore, implementations of <b>ReleaseConnection</b> should not contain blocks of code whose execution depends on whether a zero value is returned.


### -param fLastReleaseCloses [in]

This parameter is <b>TRUE</b> if the connection being released is the last external lock on the object, and therefore the object should close. Otherwise, the object should remain open until closed by the user or another process.


## -returns



The method returns the count of connections. This value is intended to be used only for debugging purposes.




## -remarks



If <i>fLastReleaseCloses</i> equals <b>TRUE</b>, calling <b>ReleaseConnection</b> causes the object to shut itself down. Calling this method is the only way in which a DLL object, running in the same process space as the container application, will know when to close following a silent update.




## -see-also




<a href="https://msdn.microsoft.com/28afc305-d5b0-4ac9-9412-5876e575c2c2">IExternalConnection</a>
 

 

