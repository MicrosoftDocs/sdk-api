---
UID: NS:wintrust._CRYPT_PROVUI_DATA
title: "_CRYPT_PROVUI_DATA"
author: windows-sdk-content
description: Provides user interface (UI) data for a provider. This structure is used by the CRYPT_PROVUI_FUNCS structure.
old-location: security\crypt_provui_data.htm
old-project: SecCrypto
ms.assetid: 86f819f0-c243-45ba-8b7b-97ed906e6e8a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*PCRYPT_PROVUI_DATA, CRYPT_PROVUI_DATA, CRYPT_PROVUI_DATA structure [Security], PCRYPT_PROVUI_DATA, PCRYPT_PROVUI_DATA structure pointer [Security], _CRYPT_PROVUI_DATA, security.crypt_provui_data, wintrust/CRYPT_PROVUI_DATA, wintrust/PCRYPT_PROVUI_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRYPT_PROVUI_DATA, *PCRYPT_PROVUI_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVUI_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _CRYPT_PROVUI_DATA structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_PROVUI_DATA</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVUI_DATA</b> structure provides user interface (UI) data for a provider. This structure is used by the <a href="https://msdn.microsoft.com/7cdc32ea-b28a-400f-ad8a-984f86bb95fd">CRYPT_PROVUI_FUNCS</a> structure.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field dwFinalError

Error code, if applicable.


### -field pYesButtonText

A pointer to a <b>null</b>-terminated string for the <b>Yes</b> button text. If this parameter is <b>NULL</b>, then "&amp;Yes" is used.


### -field pNoButtonText

A pointer to a <b>null</b>-terminated string for the <b>No</b> button text. If this parameter is <b>NULL</b>, then "&amp;No"  is used.


### -field pMoreInfoButtonText

A pointer to a <b>null</b>-terminated string for the <b>More Info</b> button text. If this parameter is <b>NULL</b>, then "&amp;More Info" is used.


### -field pAdvancedLinkText

A pointer to a <b>null</b>-terminated string for the <b>Advanced</b>  button  text.


### -field pCopyActionText

A pointer to a <b>null</b>-terminated string for the text used when the trust is valid and a time stamp is used. If this parameter is <b>NULL</b>, then "Do you want to install and run ""%1"" signed on %2 and distributed by:" is used.


### -field pCopyActionTextNoTS

A pointer to a <b>null</b>-terminated string for the text used when the trust is valid but a time stamp is not used. If this parameter is <b>NULL</b>, then "Do you want to install and run ""%1"" signed on an unknown date/time and distributed by:" is used.


### -field pCopyActionTextNotSigned

A pointer to a <b>null</b>-terminated string for the text used when a signature is not provided.  If this parameter is <b>NULL</b>, then "Do you want to install and run ""%1""?" is used.


## -see-also




<a href="https://msdn.microsoft.com/7cdc32ea-b28a-400f-ad8a-984f86bb95fd">CRYPT_PROVUI_FUNCS</a>
 

 

