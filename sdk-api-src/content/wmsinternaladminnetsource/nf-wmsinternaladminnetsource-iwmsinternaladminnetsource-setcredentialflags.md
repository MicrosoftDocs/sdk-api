---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.SetCredentialFlags
title: IWMSInternalAdminNetSource::SetCredentialFlags (wmsinternaladminnetsource.h)
description: The SetCredentialFlags method is used to set the user preference for automatic password caching.
helpviewer_keywords: ["IWMSInternalAdminNetSource interface [windows Media Format]","SetCredentialFlags method","IWMSInternalAdminNetSource.SetCredentialFlags","IWMSInternalAdminNetSource::SetCredentialFlags","IWMSInternalAdminNetSourceSetCredentialFlags","SetCredentialFlags","SetCredentialFlags method [windows Media Format]","SetCredentialFlags method [windows Media Format]","IWMSInternalAdminNetSource interface","wmformat.iwmsinternaladminnetsource_setcredentialflags","wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentialFlags"]
old-location: wmformat\iwmsinternaladminnetsource_setcredentialflags.htm
tech.root: wmformat
ms.assetid: af6208b3-84f6-44d1-9587-140044f2b2f0
ms.date: 12/05/2018
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],SetCredentialFlags method, IWMSInternalAdminNetSource.SetCredentialFlags, IWMSInternalAdminNetSource::SetCredentialFlags, IWMSInternalAdminNetSourceSetCredentialFlags, SetCredentialFlags, SetCredentialFlags method [windows Media Format], SetCredentialFlags method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_setcredentialflags, wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentialFlags
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSInternalAdminNetSource::SetCredentialFlags
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentialFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMSInternalAdminNetSource.SetCredentialFlags
---

# IWMSInternalAdminNetSource::SetCredentialFlags


## -description

The <b>SetCredentialFlags</b> method is used to set the user preference for automatic password caching. When your application prompts the user for a password, you can include a checkbox on the dialog box that the user can select to always have passwords saved. You can then set a flag to maintain that preference.

## -parameters

### -param dwFlags [in]

<b>DWORD</b> containing the credential flags. At this time, the only supported flag is 0x1, which signifies that the user has stated a preference that passwords should be saved automatically.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-getcredentialflags">IWMSInternalAdminNetSource::GetCredentialFlags</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-setcredentials">IWMSInternalAdminNetSource::SetCredentials</a>