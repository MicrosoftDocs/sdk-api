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

# tagHELPER_ATTRIBUTE structure


## -description


The <b>HELPER_ATTRIBUTE</b> structure contains all NDF supported data types.


## -struct-fields




### -field pwszName

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that contains the name of the attribute.


### -field type

Type: <b><a href="https://msdn.microsoft.com/9064549e-4f30-42f4-a7b4-6072f9c30f60">ATTRIBUTE_TYPE</a></b>

The type of helper attribute.


### -field Boolean

Type: <b>BOOL</b>

A True or False value. Used when <b>type</b> is <b>AT_BOOLEAN</b>.


### -field Char

Type: <b>char</b>

A character value. Used when  <b>type</b> is <b>AT_INT8</b>.


### -field Byte

Type: <b>byte</b>

A byte value. Used when <b>type</b> is <b>AT_UINT8</b>.


### -field Short

Type: <b>short</b>

A 16-bit  signed value. Used when <b>type</b> is <b>AT_INT16</b>


### -field Word

Type: <b>WORD</b>

A 2-byte unsigned value. Used when <b>type</b> is <b>AT_UINT16</b>.


### -field Int

Type: <b>int</b>

A 4-byte signed value. Used when <b>type</b> is <b>AT_INT32</b>.


### -field DWord

Type: <b>DWORD</b>

A 4-byte unsigned value. Used when <b>type</b> is <b>AT_UINT32</b>.


### -field Int64

Type: <b>LONGLONG</b>

A 64-bit signed integer value. Used when <b>type</b> is <b>AT_INT64</b>.


### -field UInt64

Type: <b>ULONGLONG</b>

A 64-bit unsigned integer value. Used when <b>type</b> is <b>AT_UINT64</b>.


### -field PWStr

Type: <b>LPWSTR</b>

A null-terminated string value. Used when <b>type</b> is <b>AT_STRING</b>.


### -field Guid

Type: <b>GUID</b>

A GUID structure. Used when <b>type</b> is <b>AT_GUID</b>.


### -field LifeTime

Type: <b><a href="https://msdn.microsoft.com/31f038fb-08c1-4057-af61-f3912cfcd4f0">LIFE_TIME</a></b>

A <a href="https://msdn.microsoft.com/31f038fb-08c1-4057-af61-f3912cfcd4f0">LIFE_TIME</a> structure. Used when <b>type</b> is <b>AT_LIFE_TIME</b>.


### -field Address

Type: <b><a href="https://msdn.microsoft.com/31da9541-e7d0-4cbc-9d9d-3bcf71acb975">DIAG_SOCKADDR</a></b>

An IPv4 or IPv6 address. Used when <b>type</b> is <b>AT_SOCKADDR</b>.


### -field OctetString

Type: <b><a href="https://msdn.microsoft.com/6133c69d-45ad-4080-b3e1-f42cbdc6cdf7">OCTET_STRING</a></b>

A byte array for undefined types. Used when <b>type</b> is <b>AT_OCTET_STRING</b>.


## -see-also




<a href="https://msdn.microsoft.com/9064549e-4f30-42f4-a7b4-6072f9c30f60">ATTRIBUTE_TYPE</a>



<a href="https://msdn.microsoft.com/ff49be29-4cd8-4730-929f-c66a7325704f">CopyHelperAttribute</a>



<a href="https://msdn.microsoft.com/d973bdb9-c1d1-4cea-bcc6-98671349413f">FreeHelperAttributes</a>
 

 

