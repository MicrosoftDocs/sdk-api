---
UID: NF:wsbapp.IWsbApplicationRestoreSupport.OrderComponents
title: IWsbApplicationRestoreSupport::OrderComponents (wsbapp.h)
author: windows-sdk-content
description: Specifies the order in which application components are to be restored.
old-location: wsb\iwsbapplicationrestoresupport_ordercomponents.htm
tech.root: wsb
ms.assetid: 15250479-841d-421e-8780-6dee795f29b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWsbApplicationRestoreSupport interface [Windows Server Backup],OrderComponents method, IWsbApplicationRestoreSupport.OrderComponents, IWsbApplicationRestoreSupport::OrderComponents, OrderComponents, OrderComponents method [Windows Server Backup], OrderComponents method [Windows Server Backup],IWsbApplicationRestoreSupport interface, wsb.iwsbapplicationrestoresupport_ordercomponents, wsbapp/IWsbApplicationRestoreSupport::OrderComponents
ms.topic: method
f1_keywords: 
 - "wsbapp/IWsbApplicationRestoreSupport.OrderComponents"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationRestoreSupport.OrderComponents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWsbApplicationRestoreSupport::OrderComponents


## -description


Specifies the order in which application components are to be restored.


## -parameters




### -param cComponents [in]

The number of components to be restored. The value of this parameter can range from 0 to MAX_COMPONENTS.


### -param rgComponentName [in]

An array of <i>cComponents</i> names of components to be restored.


### -param rgComponentLogicalPaths [in]

An array of <i>cComponents</i> logical paths of components to be restored.


### -param prgComponentName [out]

An array of <i>cComponents</i> names of components to be restored,  in the order in which they are to be restored. This parameter receives <b>NULL</b> if no specific restore order is required.


### -param prgComponentLogicalPath [out]

An array of <i>cComponents</i> logical paths of components to be restored, in the order in which they are to be restored. This parameter receives <b>NULL</b> if no specific restore order is required.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise. Possible return values include the following.




## -remarks



Windows Server Backup calls this  method before restoring components for an application.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wsbapp/nn-wsbapp-iwsbapplicationrestoresupport">IWsbApplicationRestoreSupport</a>
 

 

