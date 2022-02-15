---
UID: NF:shdeprecated.IBrowserService2.GetFolderSetData
title: IBrowserService2::GetFolderSetData (shdeprecated.h)
description: Deprecated. Gets a structure containing folder information.
helpviewer_keywords: ["GetFolderSetData","GetFolderSetData method [Windows Shell]","GetFolderSetData method [Windows Shell]","IBrowserService2 interface","IBrowserService2 interface [Windows Shell]","GetFolderSetData method","IBrowserService2.GetFolderSetData","IBrowserService2::GetFolderSetData","shdeprecated/IBrowserService2::GetFolderSetData","shell.IBrowserService2_GetFolderSetData","zone_IBrowserService2_GetFolderSetData"]
old-location: shell\IBrowserService2_GetFolderSetData.htm
tech.root: shell
ms.assetid: fac9323b-bf32-45d0-95c4-798a1aab4d02
ms.date: 12/05/2018
ms.keywords: GetFolderSetData, GetFolderSetData method [Windows Shell], GetFolderSetData method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetFolderSetData method, IBrowserService2.GetFolderSetData, IBrowserService2::GetFolderSetData, shdeprecated/IBrowserService2::GetFolderSetData, shell.IBrowserService2_GetFolderSetData, zone_IBrowserService2_GetFolderSetData
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::GetFolderSetData
 - shdeprecated/IBrowserService2::GetFolderSetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.GetFolderSetData
---

# IBrowserService2::GetFolderSetData


## -description

Deprecated. Gets a structure containing folder information.

## -parameters

### -param pfsd [in, out]

Type: <b>tagFolderSetData*</b>

A pointer to a <a href="/windows/desktop/api/shdeprecated/ns-shdeprecated-foldersetdata">FOLDERSETDATA</a> structure that receives the folder information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by the derived class.