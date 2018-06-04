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

# IBrowserService::OnHttpEquiv


## -description


Deprecated. Called when the document object responds to an <a href="_inet_HTTP_EQUIV_Attribute_httpEquiv_Property_scr">HTTP-EQUIV</a> metatag by issuing either the <b>OLECMDID_HTTPEQUIV</b> or <b>OLECMDID_HTTPEQUIV_DONE</b> command through <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a>.


## -parameters




### -param psv

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> that indicates the browser's view. The view must be either the browser's current view or the pending view.


### -param fDone

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates which command to issue.



#### TRUE

<b>OLECMDID_HTTPEQUIV_DONE</b>



#### FALSE

<b>OLECMDID_HTTPEQUIV</b>


### -param pvarargIn [in]

Type: <b>VARIANT*</b>

=A pointer to an object of type <b>VARIANT</b>. This is the equivalent of the <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a> parameter <i>pvaIn</i>.


### -param pvarargOut [out]

Type: <b>VARIANT*</b>

A pointer to an object of type <b>VARIANT</b>. This is the equivalent of the <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a> parameter <i>pvaOut</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



