---
UID: NF:shobjidl_core.IThumbnailHandlerFactory.GetThumbnailHandler
title: IThumbnailHandlerFactory::GetThumbnailHandler
author: windows-sdk-content
description: Gets the requested thumbnail handler for the thumbnail of a given item.
old-location: shell\IThumbnailHandlerFactory_GetThumbnailHandler.htm
old-project: shell
ms.assetid: ddd0caba-079f-4b22-8c89-6ba09adeba60
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetThumbnailHandler, GetThumbnailHandler method [Windows Shell], GetThumbnailHandler method [Windows Shell],IThumbnailHandlerFactory interface, IThumbnailHandlerFactory interface [Windows Shell],GetThumbnailHandler method, IThumbnailHandlerFactory.GetThumbnailHandler, IThumbnailHandlerFactory::GetThumbnailHandler, _shell_IThumbnailHandlerFactory_GetThumbnailHandler, shell.IThumbnailHandlerFactory_GetThumbnailHandler, shobjidl_core/IThumbnailHandlerFactory::GetThumbnailHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IThumbnailHandlerFactory.GetThumbnailHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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
      



