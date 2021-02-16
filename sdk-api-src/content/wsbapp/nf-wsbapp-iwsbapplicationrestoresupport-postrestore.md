---
UID: NF:wsbapp.IWsbApplicationRestoreSupport.PostRestore
title: IWsbApplicationRestoreSupport::PostRestore (wsbapp.h)
description: Performs application-specific PostRestore operations.
helpviewer_keywords: ["IWsbApplicationRestoreSupport interface [Windows Server Backup]","PostRestore method","IWsbApplicationRestoreSupport.PostRestore","IWsbApplicationRestoreSupport::PostRestore","PostRestore","PostRestore method [Windows Server Backup]","PostRestore method [Windows Server Backup]","IWsbApplicationRestoreSupport interface","wsb.iwsbapplicationrestoresupport_postrestore","wsbapp/IWsbApplicationRestoreSupport::PostRestore"]
old-location: wsb\iwsbapplicationrestoresupport_postrestore.htm
tech.root: wsb
ms.assetid: 8be7975e-9b94-4a6e-b1f5-794b8749ccbe
ms.date: 12/05/2018
ms.keywords: IWsbApplicationRestoreSupport interface [Windows Server Backup],PostRestore method, IWsbApplicationRestoreSupport.PostRestore, IWsbApplicationRestoreSupport::PostRestore, PostRestore, PostRestore method [Windows Server Backup], PostRestore method [Windows Server Backup],IWsbApplicationRestoreSupport interface, wsb.iwsbapplicationrestoresupport_postrestore, wsbapp/IWsbApplicationRestoreSupport::PostRestore
req.header: wsbapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsbApp.idl
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
 - IWsbApplicationRestoreSupport::PostRestore
 - wsbapp/IWsbApplicationRestoreSupport::PostRestore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationRestoreSupport.PostRestore
---

# IWsbApplicationRestoreSupport::PostRestore


## -description

Performs application-specific <a href="/windows/desktop/VSS/vssgloss-p">PostRestore</a> operations.

## -parameters

### -param wszWriterMetadata [in, optional]

A string that contains the VSS writer's metadata.

### -param wszComponentName [in, optional]

The name of the component or component set. This should match the name in the metadata that the <i>wszWriterMetadata</i> parameter points to.

### -param wszComponentLogicalPath [in, optional]

The <a href="/windows/desktop/VSS/logical-pathing-of-components">logical path</a> of the component or component set. This should match the logical path in the metadata that the <i>wszWriterMetadata</i> parameter points to.

### -param bNoRollForward [in]

Set to <b>TRUE</b> if a previous point-in-time recovery operation is in progress and no application rollforward should be performed. The previous logs for the application will be deleted before the application restore operation is performed.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise. Possible return values include the following.

## -remarks

During application restore, Windows Server Backup calls this method after restoring the files for each application component.

## -see-also

<a href="/previous-versions/windows/desktop/api/wsbapp/nn-wsbapp-iwsbapplicationrestoresupport">IWsbApplicationRestoreSupport</a>