---
UID: NE:wmsinternaladminnetsource.NETSOURCE_URLCREDPOLICY_SETTINGS
title: NETSOURCE_URLCREDPOLICY_SETTINGS (wmsinternaladminnetsource.h)
description: The NETSOURCE_URLCREDPOLICY_SETTINGS enumeration type is used for an output parameter of IWMSInternalAdminNetSource2::GetCredentialsEx.
helpviewer_keywords: ["NETSOURCE_URLCREDPOLICY_SETTINGS","NETSOURCE_URLCREDPOLICY_SETTINGS enumeration [windows Media Format]","NETSOURCE_URLCREDPOLICY_SETTING_ANONYMOUSONLY","NETSOURCE_URLCREDPOLICY_SETTING_MUSTPROMPTUSER","NETSOURCE_URLCREDPOLICY_SETTING_SILENTLOGONOK","enumeration [windows Media Format]","wmformat.netsource_urlcredpolicy_settings","wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTINGS","wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTING_ANONYMOUSONLY","wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTING_MUSTPROMPTUSER","wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTING_SILENTLOGONOK"]
old-location: wmformat\netsource_urlcredpolicy_settings.htm
tech.root: wmformat
ms.assetid: d4ffdbc8-123e-4cb4-bcc9-8d52c3362529
ms.date: 12/05/2018
ms.keywords: NETSOURCE_URLCREDPOLICY_SETTINGS, NETSOURCE_URLCREDPOLICY_SETTINGS enumeration [windows Media Format], NETSOURCE_URLCREDPOLICY_SETTING_ANONYMOUSONLY, NETSOURCE_URLCREDPOLICY_SETTING_MUSTPROMPTUSER, NETSOURCE_URLCREDPOLICY_SETTING_SILENTLOGONOK, enumeration [windows Media Format], wmformat.netsource_urlcredpolicy_settings, wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTINGS, wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTING_ANONYMOUSONLY, wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTING_MUSTPROMPTUSER, wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTING_SILENTLOGONOK
req.header: wmsinternaladminnetsource.h
req.include-header: Wminternaladminnetsource.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NETSOURCE_URLCREDPOLICY_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NETSOURCE_URLCREDPOLICY_SETTINGS
 - wmsinternaladminnetsource/NETSOURCE_URLCREDPOLICY_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmsinternaladminnetsource.h
api_name:
 - NETSOURCE_URLCREDPOLICY_SETTINGS
---

# NETSOURCE_URLCREDPOLICY_SETTINGS enumeration


## -description

The <b>NETSOURCE_URLCREDPOLICY_SETTINGS</b> enumeration type is used for an output parameter of <a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-getcredentialsex">IWMSInternalAdminNetSource2::GetCredentialsEx</a>. It specifies possible security policy settings that can exist on a client computer. When you retrieve credentials, you must proceed as dictated by the user's security preferences. For more information, see <b>GetCredentialsEx</b>.

## -enum-fields

### -field NETSOURCE_URLCREDPOLICY_SETTING_SILENTLOGONOK:0

Specifies that your application can log on to servers for which passwords are cached without informing the user.

### -field NETSOURCE_URLCREDPOLICY_SETTING_MUSTPROMPTUSER:1

Specifies that your application must notify the user when your application needs to log on to a server. You application can fill in the fields of a password dialog, but must get confirmation.

### -field NETSOURCE_URLCREDPOLICY_SETTING_ANONYMOUSONLY:2

Specifies that your application can never log on to network servers for the user. Your application can still navigate servers that do not require passwords.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
