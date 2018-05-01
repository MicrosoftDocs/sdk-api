---
UID: NF:azroles.IAzOperation.get_ApplicationData
title: IAzOperation::get_ApplicationData method
author: windows-driver-content
description: The ApplicationData property of IAzOperation sets or retrieves an opaque field that can be used by the application to store information.
old-location: security\iazoperation_applicationdata.htm
old-project: SecAuthZ
ms.assetid: d4d22aae-6ca3-4a97-aa44-fa07674dc556
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security], AzOperation object, ApplicationData property [Security], IAzOperation interface, AzOperation object [Security], ApplicationData property, IAzOperation, IAzOperation interface [Security], ApplicationData property, IAzOperation.ApplicationData, IAzOperation::get_ApplicationData, IAzOperation::put_ApplicationData, azroles/IAzOperation::ApplicationData, azroles/IAzOperation::get_ApplicationData, azroles/IAzOperation::put_ApplicationData, get_ApplicationData,IAzOperation.get_ApplicationData, security.iazoperation_applicationdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzOperation.ApplicationData
-	IAzOperation.get_ApplicationData
-	IAzOperation.put_ApplicationData
-	AzOperation.ApplicationData
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzOperation::get_ApplicationData method


## -description


The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>


