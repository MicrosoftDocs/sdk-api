---
UID: NF:wdstpdi.WdsTransportProviderCloseInstance
title: WdsTransportProviderCloseInstance function
author: windows-sdk-content
description: Closes an instance of a content provider specified by a handle.
old-location: wds\wdstransportprovidercloseinstance.htm
old-project: Wds
ms.assetid: 3eb0a931-ca5d-4db4-9c40-9c52f98be429
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WdsTransportProviderCloseInstance, WdsTransportProviderCloseInstance callback, WdsTransportProviderCloseInstance callback function [Windows Deployment Services], wds.wdstransportprovidercloseinstance, wdstpdi/WdsTransportProviderCloseInstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdstpdi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wdstpdi.h
api_name:
 - WdsTransportProviderCloseInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportProviderCloseInstance function


## -description


Closes an instance of a content provider specified by a handle. 


## -parameters




### -param hInstance [in]

Handle to the content provider instance to be closed.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



