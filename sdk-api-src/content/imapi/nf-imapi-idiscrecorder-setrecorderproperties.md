---
UID: NF:imapi.IDiscRecorder.SetRecorderProperties
title: IDiscRecorder::SetRecorderProperties (imapi.h)
author: windows-sdk-content
description: Accepts an IPropertyStorage pointer for an object with all the properties that the application wishes to change. Sparse settings are supported.
old-location: imapi\idiscrecorder_setrecorderproperties.htm
tech.root: imapi
ms.assetid: 8da0add7-6a9d-46f4-b34c-7ea9aa0b7d3a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscRecorder interface [IMAPI],SetRecorderProperties method, IDiscRecorder.SetRecorderProperties, IDiscRecorder::SetRecorderProperties, SetRecorderProperties, SetRecorderProperties method [IMAPI], SetRecorderProperties method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_setrecorderproperties, base.idiscrecorder_setrecorderproperties, imapi.idiscrecorder_setrecorderproperties, imapi/IDiscRecorder::SetRecorderProperties
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.SetRecorderProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder::SetRecorderProperties


## -description


Accepts an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> pointer for an object with all the properties that the application wishes to change. Sparse settings are supported. It is recommended, however, to query for a property set using 
<a href="https://msdn.microsoft.com/24d46cbc-56fd-4c9f-933c-0207dea5ada5">GetRecorderProperties</a>, modify only those settings of interest, and then call 
<b>SetRecorderProperties</b> to change all values simultaneously.


## -parameters




### -param pPropStg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface that the disc recorder can use to retrieve new settings on various properties.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Some properties are read-only, such as MaxWriteSpeed. Both read-only properties and unsupported properties are ignored without generating an error (see IMAPI_S_PROPERTIESIGNORED). For example, someone could submit a property set to this interface and attempt to change the MaxWriteSpeed and ClearlyNeverHeardOfBefore properties. Since MaxWriteSpeed is read-only and ClearlyNeverHeardOfBefore is an unknown value, both properties are ignored and the method succeeds.

After calling 
<b>SetRecorderProperties</b>, an application should verify property settings by calling 
<a href="https://msdn.microsoft.com/24d46cbc-56fd-4c9f-933c-0207dea5ada5">GetRecorderProperties</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

