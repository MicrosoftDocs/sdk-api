---
UID: NF:shobjidl.IPublishingWizard.GetTransferManifest
title: IPublishingWizard::GetTransferManifest (shobjidl.h)
description: Gets a transfer manifest for a file transfer operation performed by a publishing wizard, such as the Online Print Wizard or the Add Network Place Wizard.
helpviewer_keywords: ["GetTransferManifest","GetTransferManifest method [Windows Shell]","GetTransferManifest method [Windows Shell]","IPublishingWizard interface","IPublishingWizard interface [Windows Shell]","GetTransferManifest method","IPublishingWizard.GetTransferManifest","IPublishingWizard::GetTransferManifest","_shell_IPublishingWizard_GetTransferManifest","shell.IPublishingWizard_GetTransferManifest","shobjidl/IPublishingWizard::GetTransferManifest"]
old-location: shell\IPublishingWizard_GetTransferManifest.htm
tech.root: shell
ms.assetid: 1c595526-f810-4a33-82c3-785727153b16
ms.date: 12/05/2018
ms.keywords: GetTransferManifest, GetTransferManifest method [Windows Shell], GetTransferManifest method [Windows Shell],IPublishingWizard interface, IPublishingWizard interface [Windows Shell],GetTransferManifest method, IPublishingWizard.GetTransferManifest, IPublishingWizard::GetTransferManifest, _shell_IPublishingWizard_GetTransferManifest, shell.IPublishingWizard_GetTransferManifest, shobjidl/IPublishingWizard::GetTransferManifest
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Netplwiz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPublishingWizard::GetTransferManifest
 - shobjidl/IPublishingWizard::GetTransferManifest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netplwiz.dll
api_name:
 - IPublishingWizard.GetTransferManifest
---

# IPublishingWizard::GetTransferManifest


## -description

Gets a transfer manifest for a file transfer operation performed by a publishing wizard, such as the Online Print Wizard or the Add Network Place Wizard.  

            
<div class="alert"><b>Note</b>  This method is deprecated for Windows Vista, as it is not supported for Online Print Wizard or Add Network Place Wizard.</div><div> </div>

## -parameters

### -param phrFromTransfer [out]

Type: <b>HRESULT*</b>

A pointer to a variable of type <b>HRESULT</b> that, when this method returns, is set to S_OK if the transfer operation was successful, S_FALSE if the transfer has not yet begun, or a standard error value if the transfer has failed or has been canceled. This value can be <b>NULL</b> if you do not require this information.

### -param pdocManifest [out]

Type: <b>IXMLDOMDocument**</b>

Address of an <a href="/previous-versions/windows/desktop/dd892951(v=vs.85)">IXMLDOMDocument interface</a> pointer that, when this method returns, points to the <b>IXMLDOMDocument interface</b> object that represents the manifest. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the manifest is successfully retrieved or a standard COM error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The transfer manifest has not yet been created.

</td>
</tr>
</table>

## -remarks

The transfer manifest is not created until the wizard is actually displayed. For information on displaying a publishing wizard, see the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ipublishingwizard">IPublishingWizard</a> topic.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-ipublishingwizard">IPublishingWizard</a>



<a href="/windows/desktop/shell/interfaces">Transfer Manifest Schema</a>



<a href="/windows/desktop/lwef/pubwiz-manifest">Using the Transfer Manifest</a>