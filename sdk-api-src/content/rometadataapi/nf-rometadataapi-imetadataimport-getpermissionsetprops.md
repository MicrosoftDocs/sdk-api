---
UID: NF:rometadataapi.IMetaDataImport.GetPermissionSetProps
title: IMetaDataImport::GetPermissionSetProps (rometadataapi.h)
description: Gets the metadata associated with the System.Security.PermissionSet represented by the specified Permission token.
helpviewer_keywords: ["GetPermissionSetProps","GetPermissionSetProps method [Windows Runtime]","GetPermissionSetProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetPermissionSetProps method","IMetaDataImport.GetPermissionSetProps","IMetaDataImport::GetPermissionSetProps","rometadataapi/IMetaDataImport::GetPermissionSetProps","winrt.imetadataimport_getpermissionsetprops"]
old-location: winrt\imetadataimport_getpermissionsetprops.htm
tech.root: WinRT
ms.assetid: db10bdb6-3150-4eb9-872a-3f56089812fa
ms.date: 12/05/2018
ms.keywords: GetPermissionSetProps, GetPermissionSetProps method [Windows Runtime], GetPermissionSetProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetPermissionSetProps method, IMetaDataImport.GetPermissionSetProps, IMetaDataImport::GetPermissionSetProps, rometadataapi/IMetaDataImport::GetPermissionSetProps, winrt.imetadataimport_getpermissionsetprops
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
ms.custom: 19H1
f1_keywords:
 - IMetaDataImport::GetPermissionSetProps
 - rometadataapi/IMetaDataImport::GetPermissionSetProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.GetPermissionSetProps
---

# IMetaDataImport::GetPermissionSetProps


## -description

Gets the metadata associated with the <a href="/dotnet/api/system.security.permissionset">System.Security.PermissionSet</a> represented by the specified Permission token.

## -parameters

### -param tk [in]

The Permission metadata token that represents the permission set to get the metadata properties for.

### -param pdwAction [out]

A pointer to the permission set.

### -param ppvPermission [out]

A pointer to the binary metadata signature of the permission set.

### -param pcbPermission [out]

The size in bytes of <i>const</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>