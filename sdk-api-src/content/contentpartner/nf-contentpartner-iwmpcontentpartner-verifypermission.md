---
UID: NF:contentpartner.IWMPContentPartner.VerifyPermission
title: IWMPContentPartner::VerifyPermission (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","VerifyPermission method","IWMPContentPartner.VerifyPermission","IWMPContentPartner::VerifyPermission","IWMPContentPartnerVerifyPermission","VerifyPermission","VerifyPermission method [Windows Media Player]","VerifyPermission method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::VerifyPermission","wmp.iwmpcontentpartner_verifypermission"]
old-location: wmp\iwmpcontentpartner_verifypermission.htm
tech.root: WMP
ms.assetid: 7ff45264-6e49-4953-bc0a-b3652aee965d
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner interface [Windows Media Player],VerifyPermission method, IWMPContentPartner.VerifyPermission, IWMPContentPartner::VerifyPermission, IWMPContentPartnerVerifyPermission, VerifyPermission, VerifyPermission method [Windows Media Player], VerifyPermission method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::VerifyPermission, wmp.iwmpcontentpartner_verifypermission
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPContentPartner::VerifyPermission
 - contentpartner/IWMPContentPartner::VerifyPermission
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.VerifyPermission
---

# IWMPContentPartner::VerifyPermission


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>VerifyPermission</b> method initiates the process of verifying permission for Windows Media Player to perform an action.

## -parameters

### -param bstrPermission [in]

A <b>BSTR</b> that specifies the action for which permission is being requested. See Remarks for a list of possible values.

### -param pContext [in]

A pointer to a <b>VARIANT</b> that contains information related to the request. See Remarks.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The <b>VerifyPermission</b> method initiates a permission verification and then returns immediately. When the online store has completed the verification, it calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-verifypermissioncomplete">IWMPContentPartnerCallback::VerifyPermissionComplete</a> to notify Windows Media Player that permission has been granted or denied.

The following list gives the possible values for <i>bstrPermission</i> along with the corresponding meanings of <i>pContext</i>.

g_szVerifyPermissionSync

Windows Media Player is requesting permission from the online store to synchronize the content on a portable device. The <i>pContext</i> parameter is a <b>VT_BSTR</b> that specifies the canonical device name.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-verifypermissioncomplete">IWMPContentPartnerCallback::VerifyPermissionComplete</a>