---
UID: NF:imapi.IDiscRecorder.GetRecorderProperties
title: IDiscRecorder::GetRecorderProperties
author: windows-sdk-content
description: Retrieves a pointer to an IPropertyStorage interface.
old-location: imapi\idiscrecorder_getrecorderproperties.htm
old-project: imapi
ms.assetid: 24d46cbc-56fd-4c9f-933c-0207dea5ada5
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: GetRecorderProperties, GetRecorderProperties method [IMAPI], GetRecorderProperties method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetRecorderProperties method, IDiscRecorder.GetRecorderProperties, IDiscRecorder::GetRecorderProperties, _win32_idiscrecorder_getrecorderproperties, base.idiscrecorder_getrecorderproperties, imapi.idiscrecorder_getrecorderproperties, imapi/IDiscRecorder::GetRecorderProperties
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.GetRecorderProperties
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder::GetRecorderProperties


## -description


Retrieves a pointer to an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface.


## -parameters




### -param ppPropStg






#### - pPropStg [out]

Pointer to an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface to the property set with all current properties defined.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Properties are not retained after IMAPI is closed. A property set format is convenient for IMAPI because it stores an ID/TYPE/VALUE combination, as well as ID/NAME associations. Each combination is a single property, and IMAPI uses these properties for various values that are unique to specific recorders. For example, most recorders would support a WriteSpeed property.

The caller can then modify properties by calling 
<a href="https://msdn.microsoft.com/8da0add7-6a9d-46f4-b34c-7ea9aa0b7d3a">SetRecorderProperties</a>. Current properties include the following:






## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>
 

 

