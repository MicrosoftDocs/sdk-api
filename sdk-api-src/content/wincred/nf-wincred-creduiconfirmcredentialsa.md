---
UID: NF:wincred.CredUIConfirmCredentialsA
title: CredUIConfirmCredentialsA function (wincred.h)
description: Is called after CredUIPromptForCredentials or CredUICmdLinePromptForCredentials, to confirm the validity of the credential harvested. (ANSI)
helpviewer_keywords: ["CredUIConfirmCredentialsA", "wincred/CredUIConfirmCredentialsA"]
old-location: security\creduiconfirmcredentials.htm
tech.root: security
ms.assetid: 67262844-75f0-4f68-90f6-63f9a6d2b0a1
ms.date: 12/05/2018
ms.keywords: CredUIConfirmCredentials, CredUIConfirmCredentials function [Security], CredUIConfirmCredentialsA, CredUIConfirmCredentialsW, _cred_creduiconfirmcredentials, security.creduiconfirmcredentials, wincred/CredUIConfirmCredentials, wincred/CredUIConfirmCredentialsA, wincred/CredUIConfirmCredentialsW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUIConfirmCredentialsW (Unicode) and CredUIConfirmCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredUIConfirmCredentialsA
 - wincred/CredUIConfirmCredentialsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-0.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUIConfirmCredentials
 - CredUIConfirmCredentialsA
 - CredUIConfirmCredentialsW
---

# CredUIConfirmCredentialsA function


## -description

The <b>CredUIConfirmCredentials</b> function is called after 
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> or 
<a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a>, to confirm the validity of the credential harvested. <b>CredUIConfirmCredentials</b> must be called if the CREDUI_FLAGS_EXPECT_CONFIRMATION flag was passed to the "prompt" function, either <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> or <a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a>, and the "prompt" function returned NO_ERROR.

After calling the "prompt" function and before calling <b>CredUIConfirmCredentials</b>, the caller must determine whether the credentials are actually valid by using the credentials to access the resource specified by <i>pszTargetName</i>. The results of that validation test are passed to <b>CredUIConfirmCredentials</b> in the <i>bConfirm</i> parameter.

## -parameters

### -param pszTargetName [in]

Pointer to a <b>null</b>-terminated string that contains the name of the target for the credentials, typically a domain or server application name. This must be the same value passed as <i>pszTargetName</i> to <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> or <a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a>

### -param bConfirm [in]

Specifies whether the credentials returned from the prompt function are valid. If <b>TRUE</b>, the credentials are stored in the credential manager as defined by <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> or <a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a>. If <b>FALSE</b>, the credentials are not stored and various pieces of memory are cleaned up.

## -returns

Status of the operation is returned. The caller can check this status to determine whether the credential confirm operation succeeded. Most applications ignore this status code because the application's connection to the resource has already been done. The operation can fail because the credential was not found on the list of credentials awaiting confirmation, or because the attempt to write or delete the credential failed. Failure to find the credential on the list can occur because the credential was never queued or as a result of too many credentials being queued. Up to five credentials can be queued before older ones are discarded as newer ones are queued.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR - (zero)</b></dt>
</dl>
</td>
<td width="60%">
Confirm operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The subject credential could not be found on the confirmation waiting list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An attempt to confirm a waiting credential failed because the credential contained data that was not valid or was inconsistent.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The wincred.h header defines CredUIConfirmCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
