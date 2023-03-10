---
UID: NF:thumbcache.IThumbnailSettings.SetContext
title: IThumbnailSettings::SetContext (thumbcache.h)
description: Enables a thumbnail provider to return a thumbnail specific to the user's context.
helpviewer_keywords: ["IThumbnailSettings interface [Windows Shell]","SetContext method","IThumbnailSettings.SetContext","IThumbnailSettings::SetContext","SetContext","SetContext method [Windows Shell]","SetContext method [Windows Shell]","IThumbnailSettings interface","shell.IThumbnailSettings_SetContext","thumbcache/IThumbnailSettings::SetContext"]
old-location: shell\IThumbnailSettings_SetContext.htm
tech.root: shell
ms.assetid: AD333075-3358-4fee-BDEE-087B7012C93E
ms.date: 12/05/2018
ms.keywords: IThumbnailSettings interface [Windows Shell],SetContext method, IThumbnailSettings.SetContext, IThumbnailSettings::SetContext, SetContext, SetContext method [Windows Shell], SetContext method [Windows Shell],IThumbnailSettings interface, shell.IThumbnailSettings_SetContext, thumbcache/IThumbnailSettings::SetContext
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
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
ms.custom: 19H1
f1_keywords:
 - IThumbnailSettings::SetContext
 - thumbcache/IThumbnailSettings::SetContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - IThumbnailSettings.SetContext
---

# IThumbnailSettings::SetContext


## -description

Enables a thumbnail provider to return a thumbnail specific to the user's context.

Initially, a thumbnail provider receives a request for a thumbnail image through a call to the <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a> method. In response, before the provider calls <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-extract">IExtractImage::Extract</a> or <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail">IThumbnailProvider::GetThumbnail</a>, the thumbnail cache can call <b>IThumbnailSettings::SetContext</b> to ensure that the thumbnail that is returned is appropriate to the user's context. For example, the provider could detect the new <b>WTS_APPSTYLE</b> flag and return a thumbnail that conforms to the Windows 8 UI guidelines.

## -parameters

### -param dwContext [in]

Type: <b><a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_contextflags">WTS_CONTEXTFLAGS</a></b>

One or more flags that specify the context. This value is based on the <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_FLAGS</a> values that are received by the thumbnail provider through the call to <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail">IThumbnailProvider::GetThumbnail</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailsettings">IThumbnailSettings</a>