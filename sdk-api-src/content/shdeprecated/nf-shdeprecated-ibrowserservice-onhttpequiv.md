---
UID: NF:shdeprecated.IBrowserService.OnHttpEquiv
title: IBrowserService::OnHttpEquiv
author: windows-sdk-content
description: Deprecated. Called when the document object responds to an HTTP-EQUIV metatag by issuing either the OLECMDID_HTTPEQUIV or OLECMDID_HTTPEQUIV_DONE command through IOleCommandTarget::Exec.
old-location: shell\IBrowserService_OnHttpEquiv.htm
tech.root: shell
ms.assetid: 9920c08b-c0c3-4359-9c00-3a1063cea0c7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FALSE, IBrowserService interface [Windows Shell],OnHttpEquiv method, IBrowserService.OnHttpEquiv, IBrowserService::OnHttpEquiv, OnHttpEquiv, OnHttpEquiv method [Windows Shell], OnHttpEquiv method [Windows Shell],IBrowserService interface, TRUE, shdeprecated/IBrowserService::OnHttpEquiv, shell.IBrowserService_OnHttpEquiv, zone_IBrowserService_OnHttpEquiv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - Shdeprecated.h
api_name:
 - IBrowserService.OnHttpEquiv
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::OnHttpEquiv


## -description


Deprecated. Called when the document object responds to an <a href="https://msdn.microsoft.com/library/ms533876(v=VS.85).aspx">HTTP-EQUIV</a> metatag by issuing either the <b>OLECMDID_HTTPEQUIV</b> or <b>OLECMDID_HTTPEQUIV_DONE</b> command through <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a>.


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



