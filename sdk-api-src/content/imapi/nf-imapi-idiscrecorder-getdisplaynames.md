---
UID: NF:imapi.IDiscRecorder.GetDisplayNames
title: IDiscRecorder::GetDisplayNames
author: windows-sdk-content
description: Retrieves a formatted name for the recorder that can be displayed. The name consists of the manufacturer and product identifier of the device.
old-location: imapi\idiscrecorder_getdisplaynames.htm
tech.root: imapi
ms.assetid: 0f20cae4-3f9c-49bb-9b82-13351b889a31
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDisplayNames, GetDisplayNames method [IMAPI], GetDisplayNames method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetDisplayNames method, IDiscRecorder.GetDisplayNames, IDiscRecorder::GetDisplayNames, _win32_idiscrecorder_getdisplaynames, base.idiscrecorder_getdisplaynames, imapi.idiscrecorder_getdisplaynames, imapi/IDiscRecorder::GetDisplayNames
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDiscRecorder.GetDisplayNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder::GetDisplayNames


## -description


Retrieves a formatted name for the recorder that can be displayed. The name consists of the manufacturer and product identifier of the device.


## -parameters




### -param pbstrVendorID [out]

Vendor of the disc recorder. This parameter can be <b>NULL</b>.


### -param pbstrProductID [out]

Product name of the disc recorder. This parameter can be <b>NULL</b>.


### -param pbstrRevision [out]

Revision of the disc recorder. This is typically the revision of the recorder firmware, but it can be a revision for the entire device. This parameter can be <b>NULL</b>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



The display names are typically combined into a string that is displayed in recorder selection list boxes or other GUI components.

The combination of these three strings does not produce a unique identifier for this specific recorder. Combine these strings with the string returned from 
<a href="https://msdn.microsoft.com/bceb7302-e5e6-4ee5-9adb-1736ab62e819">GetPath</a> to create a unique value.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

