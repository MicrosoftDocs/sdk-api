---
UID: NS:setupapi._SP_DEVINFO_DATA
title: "_SP_DEVINFO_DATA"
author: windows-sdk-content
description: An SP_DEVINFO_DATA structure defines a device instance that is a member of a device information set.
old-location: devinst\sp_devinfo_data.htm
old-project: devinst
ms.assetid: 9ad0ef4f-4a67-4f16-8bb1-2242dad0d041
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PSP_DEVINFO_DATA, PSP_DEVINFO_DATA, PSP_DEVINFO_DATA structure pointer [Device and Driver Installation], SP_DEVINFO_DATA, SP_DEVINFO_DATA structure [Device and Driver Installation], _SP_DEVINFO_DATA, devinst.sp_devinfo_data, di-struct_1d8e747e-8359-405d-8819-29c516a99cbe.xml, setupapi/PSP_DEVINFO_DATA, setupapi/SP_DEVINFO_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: SP_DEVINFO_DATA, *PSP_DEVINFO_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVINFO_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SP_DEVINFO_DATA structure


## -description


An SP_DEVINFO_DATA structure defines a device instance that is a member of a device information set.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_DEVINFO_DATA structure. For more information, see the following Remarks section.


### -field ClassGuid

The GUID of the device's setup class.


### -field DevInst

An opaque handle to the device instance (also known as a handle to the <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>). 

Some functions, such as <b>SetupDi</b><i>Xxx</i> functions, take the whole SP_DEVINFO_DATA structure as input to identify a device in a device information set. Other functions, such as <b>CM</b>_<i>Xxx</i> functions like <a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a>, take this <b>DevInst</b> handle as input.


### -field Reserved

Reserved. For internal use only.


## -remarks



An SP_DEVINFO_DATA structure identifies a device in a device information set. For example, when Windows sends a <a href="https://msdn.microsoft.com/2d369086-c2b6-45a4-a87e-51ff5725938f">DIF_INSTALLDEVICE</a> request to a class installer and co-installers, it includes a handle to a device information set and a pointer to an SP_DEVINFO_DATA that specifies the particular device. In addition to DIF requests, this structure is also used in some <b>SetupDi</b><i>Xxx</i> functions.

<b>SetupDi</b><i>Xxx</i> functions that take an SP_DEVINFO_DATA structure as a parameter verify that the <b>cbSize</b> member of the supplied structure is equal to the size, in bytes, of the structure. If the <b>cbSize</b> member is not set correctly for an input parameter, the function will fail and set an error code of ERROR_INVALID_PARAMETER. If the <b>cbSize</b> member is not set correctly for an output parameter, the function will fail and set an error code of ERROR_INVALID_USER_BUFFER. 




## -see-also




<a href="https://msdn.microsoft.com/03e6c137-5a7f-443d-878f-5e5c6642dde9">SP_DEVINFO_LIST_DETAIL_DATA</a>
 

 

