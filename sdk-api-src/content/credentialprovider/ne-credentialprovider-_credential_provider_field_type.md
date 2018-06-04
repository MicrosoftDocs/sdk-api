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

# _CREDENTIAL_PROVIDER_FIELD_TYPE enumeration


## -description


Specifies a type of credential field. Used by <a href="https://msdn.microsoft.com/8409b4b7-c601-4e85-95f9-4272feb29028">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a>.


## -enum-fields




### -field CPFT_INVALID

The value is invalid. This is a safe initialization value, as fields do not default to any given type.


### -field CPFT_LARGE_TEXT

A stand-alone text label is drawn in the larger of two font sizes.


### -field CPFT_SMALL_TEXT

A stand-alone text label is drawn in the smaller of two font sizes.


### -field CPFT_COMMAND_LINK

An uneditable string that a user may click to perform an action. The credential provider is informed of the user's click, and then performs the requested action. Use <a href="https://msdn.microsoft.com/04e371cb-f968-4a15-9285-e676dff59899">CommandLinkClicked</a> in your credential provider to respond to the click.


### -field CPFT_EDIT_TEXT

An edit box. Users may provide credential information by typing in this box.


### -field CPFT_PASSWORD_TEXT

A special edit control that displays its string as a series of password characters, such as the asterisk character (*). Otherwise this functions the same as <b>CPFT_EDIT_TEXT</b>.


### -field CPFT_TILE_IMAGE

A bitmap that is shown as the user tile image. This bitmap cannot be edited. All credential providers must contain no more than one <b>CPFT_TILE_IMAGE</b>. If no image is specified, Logon UI and Credential UI will supply a default tile image.


### -field CPFT_CHECKBOX

A checkbox control that allows for checked and unchecked states.


### -field CPFT_COMBOBOX

A combobox control that allows users to select an option from a defined set of choices.


### -field CPFT_SUBMIT_BUTTON

This field appears as a button on the credential tile. Pressing the button lets the user submit their credentials. There is exactly one <b>CPFT_SUBMIT_BUTTON</b> on any credential tile. Unlike Logon UI, which draws a special submit button in the tile layout, Credential UI hides this field and renders a single submit button for all credentials.


## -remarks



This type enables you to specify the different elements your credential provider will need to display to the user. Credential providers are not responsible for drawing their own UI, so they need to define the elements that are necessary. This type is one of the elements to support that mechanism.



