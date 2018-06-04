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
 

 

