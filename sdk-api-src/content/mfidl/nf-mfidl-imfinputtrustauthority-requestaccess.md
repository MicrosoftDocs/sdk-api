---
UID: NF:mfidl.IMFInputTrustAuthority.RequestAccess
title: IMFInputTrustAuthority::RequestAccess (mfidl.h)
description: Requests permission to perform a specified action on the stream.
helpviewer_keywords: ["8f2f7f65-7000-4404-8678-ba36c5c97c80","IMFInputTrustAuthority interface [Media Foundation]","RequestAccess method","IMFInputTrustAuthority.RequestAccess","IMFInputTrustAuthority::RequestAccess","RequestAccess","RequestAccess method [Media Foundation]","RequestAccess method [Media Foundation]","IMFInputTrustAuthority interface","mf.imfinputtrustauthority_requestaccess","mfidl/IMFInputTrustAuthority::RequestAccess"]
old-location: mf\imfinputtrustauthority_requestaccess.htm
tech.root: mf
ms.assetid: 8f2f7f65-7000-4404-8678-ba36c5c97c80
ms.date: 12/05/2018
ms.keywords: 8f2f7f65-7000-4404-8678-ba36c5c97c80, IMFInputTrustAuthority interface [Media Foundation],RequestAccess method, IMFInputTrustAuthority.RequestAccess, IMFInputTrustAuthority::RequestAccess, RequestAccess, RequestAccess method [Media Foundation], RequestAccess method [Media Foundation],IMFInputTrustAuthority interface, mf.imfinputtrustauthority_requestaccess, mfidl/IMFInputTrustAuthority::RequestAccess
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFInputTrustAuthority::RequestAccess
 - mfidl/IMFInputTrustAuthority::RequestAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFInputTrustAuthority.RequestAccess
---

# IMFInputTrustAuthority::RequestAccess


## -description

Requests permission to perform a specified action on the stream.

## -parameters

### -param Action [in]

The requested action, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfpolicymanager_action">MFPOLICYMANAGER_ACTION</a> enumeration.

### -param ppContentEnablerActivate [out]

Receives the value <b>NULL</b> or a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. The <b>IMFActivate</b> interface is used to create a content enabler object. The caller must release the interface. For more information, see Remarks.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
The user has permission to perform this action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_NEEDS_INDIVIDUALIZATION</b></dt>
</dl>
</td>
<td width="60%">
The user must individualize the application.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_LICENSE_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The user must obtain a license.

</td>
</tr>
</table>

## -remarks

This method verifies whether the user has permission to perform a specified action on the stream. The ITA does any work needed to verify the user's right to perform the action, such as checking licenses.

To verify the user's rights, the ITA might need to perform additional steps that require interaction with the user or consent from the user. For example, it might need to acquire a new license or individualize a DRM component. In that case, the ITA creates an activation object for a content enabler and returns the activation object's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface in the <i>ppContentEnablerActivate</i> parameter. The activation object is responsible for creating a content enabler that exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a> interface. The content enabler is used as follows:

<ol>
<li>
The Media Session returns the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer to the application.

</li>
<li>
The application calls <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> to activate the content enabler.

</li>
<li>
The application calls <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a> methods to perform whatever actions are needed, such as individualization or obtaining a license. The content enabler object must encapsulate this functionality through the <b>IMFContentEnabler</b> interface.

</li>
<li>
The Media Session calls <b>RequestAccess</b> again.

</li>
</ol>
The return value signals whether the user has permission to perform the action:

<ul>
<li>
If the user already has permission to perform the action, the method returns S_OK and sets *<i>ppContentEnablerActivate</i> to <b>NULL</b>.

</li>
<li>
If the user does not have permission, the method returns a failure code and sets *<i>ppContentEnablerActivate</i> to <b>NULL</b>.

</li>
<li>
If the ITA must perform additional steps that require interaction with the user, the method returns a failure code and returns the content enabler's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer in <i>ppContentEnablerActivate</i>.

</li>
</ul>
The Media Session will not allow the action unless this method returns S_OK. However, a return value of S_OK does not guarantee that the action will be performed, because some other failure might occur after this method is called. When the action is definitely about to happen, the Media Session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-bindaccess">IMFInputTrustAuthority::BindAccess</a>.

A stream can go to multiple outputs, so this method might be called multiple times with different actions, once for every output.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>