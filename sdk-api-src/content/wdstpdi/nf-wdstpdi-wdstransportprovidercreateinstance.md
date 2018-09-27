---
UID: NF:wdstpdi.WdsTransportProviderCreateInstance
title: WdsTransportProviderCreateInstance function
author: windows-sdk-content
description: Opens a new instance of a content provider.
old-location: wds\wdstransportprovidercreateinstance.htm
tech.root: wds
ms.assetid: 534ba680-e5d7-47e7-83ad-2b621feab99f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WdsTransportProviderCreateInstance, WdsTransportProviderCreateInstance callback, WdsTransportProviderCreateInstance callback function [Windows Deployment Services], wds.wdstransportprovidercreateinstance, wdstpdi/WdsTransportProviderCreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdstpdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - wdstpdi.h
api_name:
 - WdsTransportProviderCreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsTransportProviderCreateInstance function


## -description


Opens a new instance of a content provider.


## -parameters




### -param pwszConfigString [in]

Configuration information for this instance of the content provider.


### -param phInstance [out]

Receives a pointer to a handle that identifies this instance.  When the instance is no longer needed, the handle should be closed with the <a href="https://msdn.microsoft.com/3eb0a931-ca5d-4db4-9c40-9c52f98be429">WdsTransportProviderCloseInstance</a> callback. 


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



