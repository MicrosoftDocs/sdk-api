---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IThumbnailHandlerFactory::GetThumbnailHandler


## -description


Gets the requested thumbnail handler for the thumbnail of a given item.


## -parameters




### -param pidlChild [in]

Type: <b>PCUITEMID_CHILD</b>

The item within the namespace for which the thumbnail handler is being retrieved.


### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> to be used during the moniker binding operation of this process.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface requested. This is usually <a href="https://msdn.microsoft.com/55c4739a-4835-4f53-a435-804ddf06ffcf">IThumbnailProvider</a> or <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the requested thumbnail handler. If this method fails, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        Windows Vista calls the <b>IThumbnailHandlerFactory::GetThumbnailHandler</b> method before falling back on <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">GetUIObjectOf</a>.
      



