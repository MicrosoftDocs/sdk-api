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

# CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS enumeration


## -description


Provides customization options for a single field in a logon or credential UI. Used by <a href="https://msdn.microsoft.com/5507E8DE-5746-4031-900B-3EF5C97BC2EE">ICredentialProviderCredentialEvents2::SetFieldOptions</a> and <a href="https://msdn.microsoft.com/DE5E6F0E-F4FD-43ce-A1EB-F45C04C85239">ICredentialProviderCredentialWithFieldOptions::GetFieldOptions</a>.


## -enum-fields




### -field CPCFO_NONE


### -field CPCFO_ENABLE_PASSWORD_REVEAL


### -field CPCFO_IS_EMAIL_ADDRESS


### -field CPCFO_ENABLE_TOUCH_KEYBOARD_AUTO_INVOKE

When enabled, the touch keyboard will be automatically invoked. This should be set only on the <b>CPFG_CREDENTIAL_PROVIDER_LOGO</b> field.


### -field CPCFO_NUMBERS_ONLY

The field will only allow numerals to be entered. The on-screen keyboard should be optimized for that input (showing only a number keypad on the primary keyboard layout). This should be set only on the <b>CPFT_PASSWORD_TEXT</b> field 


### -field CPCFO_SHOW_ENGLISH_KEYBOARD




#### - CPCFPO_ENABLE_PASSWORD_REVEAL

Display the "password reveal" glyph in a password entry box. When this glyph is held down by the user, the entry in the password box is shown in plain text. The glyph is shown here:

                        

<img alt="Password reveal glyph" src="images/PasswordReveal.png"/>


#### - CPCFPO_IS_EMAIL_ADDRESS

The field will contain an e-mail address. The on-screen keyboard should be optimized for that input (showing the .com and @ keys on the primary keyboard layout). This option is used with Microsoft account credentials.


#### - CPCFPO_NONE

Default. Do not show the "password reveal" glyph and use the standard on-screen keyboard layout.


## -see-also




<a href="https://msdn.microsoft.com/5507E8DE-5746-4031-900B-3EF5C97BC2EE">ICredentialProviderCredentialEvents2::SetFieldOptions</a>



<a href="https://msdn.microsoft.com/DE5E6F0E-F4FD-43ce-A1EB-F45C04C85239">ICredentialProviderCredentialWithFieldOptions::GetFieldOptions</a>
 

 

