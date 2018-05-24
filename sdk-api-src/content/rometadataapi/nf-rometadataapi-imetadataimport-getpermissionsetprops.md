---
UID: NF:rometadataapi.IMetaDataImport.GetPermissionSetProps
title: IMetaDataImport::GetPermissionSetProps
author: windows-driver-content
description: Gets the metadata associated with the System.Security.PermissionSet represented by the specified Permission token.
old-location: winrt\imetadataimport_getpermissionsetprops.htm
old-project: WinRT
ms.assetid: db10bdb6-3150-4eb9-872a-3f56089812fa
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetPermissionSetProps, GetPermissionSetProps method [Windows Runtime], GetPermissionSetProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetPermissionSetProps method, IMetaDataImport.GetPermissionSetProps, IMetaDataImport::GetPermissionSetProps, rometadataapi/IMetaDataImport::GetPermissionSetProps, winrt.imetadataimport_getpermissionsetprops
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.GetPermissionSetProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport::GetPermissionSetProps


## -description


Gets the metadata associated with the <a href="http://msdn.microsoft.com/en-us/library/system.security.permissionset.aspx">System.Security.PermissionSet</a> represented by the specified Permission token.


## -parameters




### -param tk [in]

The Permission metadata token that represents the permission set to get the metadata properties for.


### -param pdwAction [out]

A pointer to the permission set.


### -param ppvPermission




### -param pcbPermission [out]

The size in bytes of <i>const</i>.


#### - const [out]

A pointer to the binary metadata signature of the permission set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

