---
UID: NF:cfapi.CfGetSyncRootInfoByHandle
title: CfGetSyncRootInfoByHandle function
author: windows-driver-content
description: Gets various characteristics of the sync root containing a given file specified by a file handle.
old-location: cloudapi\cfgetsyncrootinfobyhandle.htm
old-project: cfApi
ms.assetid: EC96CB4E-6BCE-49D9-9CDA-A24A9303B5CF
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CfGetSyncRootInfoByHandle, CfGetSyncRootInfoByHandle function, cfapi/CfGetSyncRootInfoByHandle, cloudApi.cfgetsyncrootinfobyhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CF_PLACEHOLDER_RANGE_INFO_CLASS, *PCF_PLACEHOLDER_RANGE_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CldApi.dll
api_name:
-	CfGetSyncRootInfoByHandle
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfGetSyncRootInfoByHandle function


## -description


Gets various characteristics of the sync root containing a given file specified by a file handle.


## -parameters




### -param FileHandle [in]

Handle of the file under the sync root whose information is to be queried.


### -param InfoClass [in]

Types of sync root information.


### -param InfoBuffer [out]

A pointer to a buffer that will receive the sync root information.


### -param InfoBufferLength [in]

Length, in bytes, of the <i>InfoBuffer</i>.


### -param ReturnedLength [out, optional]

The number of bytes returned in the <i>InfoBuffer</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Unlike most placeholder APIs that take a file handle, this one does not modify the file in any way, therefore the file handle only requires READ_ATTRIBUTES access.



