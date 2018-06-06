---
UID: NC:resapi.PRESUTIL_ENUM_PROPERTIES
title: PRESUTIL_ENUM_PROPERTIES
author: windows-sdk-content
description: Enumerates the property names of a cluster object. The PRESUTIL_ENUM_PROPERTIES type defines a pointer to this function.
old-location: mscs\resutilenumproperties.htm
old-project: MsCS
ms.assetid: 1b3a6326-c0da-470a-9cd5-19daa9d48ccd
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PRESUTIL_ENUM_PROPERTIES, PRESUTIL_ENUM_PROPERTIES callback, PRESUTIL_ENUM_PROPERTIES callback function [Failover Cluster], _wolf_resutilenumproperties, mscs.resutilenumproperties, resapi/PRESUTIL_ENUM_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_ENUM_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_ENUM_PROPERTIES callback function


## -description


Enumerates the property names of a  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>. The <b>PRESUTIL_ENUM_PROPERTIES</b> type defines a pointer to this function.


## -parameters




### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing properties to enumerate.


### -param pszOutProperties [out]

Pointer to the output buffer in which to return the names of all of the properties in multiple string format. Each property name is stored as a null-terminated Unicode string. The last property name is followed by a final null-terminating character.


### -param cbOutPropertiesSize [in]

Size in bytes of the output buffer pointed to by <i>pszOutProperties</i>.


### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>pszOutProperties</i>.


### -param pcbRequired [out]

Number of bytes required if the output buffer is too small.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 

