---
UID: NF:shdeprecated.IBrowserService.OnHttpEquiv
title: IBrowserService::OnHttpEquiv (shdeprecated.h)
description: Deprecated. Called when the document object responds to an HTTP-EQUIV metatag by issuing either the OLECMDID_HTTPEQUIV or OLECMDID_HTTPEQUIV_DONE command through IOleCommandTarget::Exec.
helpviewer_keywords: ["FALSE","IBrowserService interface [Windows Shell]","OnHttpEquiv method","IBrowserService.OnHttpEquiv","IBrowserService::OnHttpEquiv","OnHttpEquiv","OnHttpEquiv method [Windows Shell]","OnHttpEquiv method [Windows Shell]","IBrowserService interface","TRUE","shdeprecated/IBrowserService::OnHttpEquiv","shell.IBrowserService_OnHttpEquiv","zone_IBrowserService_OnHttpEquiv"]
old-location: shell\IBrowserService_OnHttpEquiv.htm
tech.root: shell
ms.assetid: 9920c08b-c0c3-4359-9c00-3a1063cea0c7
ms.date: 12/05/2018
ms.keywords: FALSE, IBrowserService interface [Windows Shell],OnHttpEquiv method, IBrowserService.OnHttpEquiv, IBrowserService::OnHttpEquiv, OnHttpEquiv, OnHttpEquiv method [Windows Shell], OnHttpEquiv method [Windows Shell],IBrowserService interface, TRUE, shdeprecated/IBrowserService::OnHttpEquiv, shell.IBrowserService_OnHttpEquiv, zone_IBrowserService_OnHttpEquiv
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::OnHttpEquiv
 - shdeprecated/IBrowserService::OnHttpEquiv
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.OnHttpEquiv
---

# IBrowserService::OnHttpEquiv


## -description

Deprecated. Called when the document object responds to an <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes">HTTP-EQUIV</a> metatag by issuing either the <b>OLECMDID_HTTPEQUIV</b> or <b>OLECMDID_HTTPEQUIV_DONE</b> command through <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a>.

## -parameters

### -param psv

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> that indicates the browser's view. The view must be either the browser's current view or the pending view.

### -param fDone

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates which command to issue.



#### TRUE

<b>OLECMDID_HTTPEQUIV_DONE</b>



#### FALSE

<b>OLECMDID_HTTPEQUIV</b>

### -param pvarargIn [in]

Type: <b>VARIANT*</b>

=A pointer to an object of type <b>VARIANT</b>. This is the equivalent of the <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a> parameter <i>pvaIn</i>.

### -param pvarargOut [out]

Type: <b>VARIANT*</b>

A pointer to an object of type <b>VARIANT</b>. This is the equivalent of the <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a> parameter <i>pvaOut</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.