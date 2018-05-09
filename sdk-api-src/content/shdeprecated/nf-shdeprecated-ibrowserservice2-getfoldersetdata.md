---
UID: NF:shdeprecated.IBrowserService2.GetFolderSetData
title: IBrowserService2::GetFolderSetData
author: windows-driver-content
description: Deprecated. Gets a structure containing folder information.
old-location: shell\IBrowserService2_GetFolderSetData.htm
old-project: shell
ms.assetid: fac9323b-bf32-45d0-95c4-798a1aab4d02
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetFolderSetData, GetFolderSetData method [Windows Shell], GetFolderSetData method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetFolderSetData method, IBrowserService2.GetFolderSetData, IBrowserService2::GetFolderSetData, shdeprecated/IBrowserService2::GetFolderSetData, shell.IBrowserService2_GetFolderSetData, zone_IBrowserService2_GetFolderSetData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService2.GetFolderSetData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::GetFolderSetData


## -description


Deprecated. Gets a structure containing folder information.


## -parameters




### -param pfsd [in, out]

Type: <b>tagFolderSetData*</b>

A pointer to a <a href="https://msdn.microsoft.com/eb47cd77-5788-4130-8d9c-cc84582e5d8e">FOLDERSETDATA</a> structure that receives the folder information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by the derived class.



