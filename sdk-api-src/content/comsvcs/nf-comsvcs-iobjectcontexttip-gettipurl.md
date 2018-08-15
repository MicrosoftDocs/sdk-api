---
UID: NF:comsvcs.IObjectContextTip.GetTipUrl
title: IObjectContextTip::GetTipUrl
author: windows-sdk-content
description: Retrieves the URL of the TIP context.
old-location: cos\iobjectcontexttip_gettipurl.htm
old-project: cossdk
ms.assetid: 9948a1b4-efbe-4a44-a67d-ea91a846708f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTipUrl, GetTipUrl method [COM+], GetTipUrl method [COM+],IObjectContextTip interface, IObjectContextTip interface [COM+],GetTipUrl method, IObjectContextTip.GetTipUrl, IObjectContextTip::GetTipUrl, _cos_IObjectContextTip_GetTipUrl, comsvcs/IObjectContextTip::GetTipUrl, cos.iobjectcontexttip_gettipurl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectContextTip.GetTipUrl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjectContextTip::GetTipUrl


## -description


Retrieves the URL of the TIP context.


## -parameters




### -param pTipUrl [out, retval]

The URL of the TIP transaction context, or <b>NULL</b> if the transaction context does not exist.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2fe4de87-e7ea-4120-8e37-5a26d836fcea">IObjectContextTip</a>
 

 

