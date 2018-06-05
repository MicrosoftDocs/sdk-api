---
UID: NF:mfidl.MFGetLocalId
title: MFGetLocalId function
author: windows-sdk-content
description: Gets the local system ID.
old-location: mf\mfgetlocalid.htm
old-project: medfound
ms.assetid: 24EA8907-9EBF-42FF-8823-05D48E27F9EA
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFGetLocalId, MFGetLocalId function [Media Foundation], mf.mfgetlocalid, mfidl/MFGetLocalId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFGetLocalId
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFGetLocalId function


## -description


Gets the local system ID.


## -parameters




### -param verifier [in]

Application-specific verifier value.


### -param size

Length in bytes of verifier.


### -param id [in]

Returned ID string.  This value must be freed by the caller by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

