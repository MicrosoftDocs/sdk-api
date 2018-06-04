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

# ASSOCIATIONTYPE enumeration


## -description


Specifies the type of association for an application. Used by methods of the <a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a> interface.


## -enum-fields




### -field AT_FILEEXTENSION

Indicates a file name extension, such as <code>.htm</code> or <code>.mp3</code>.


### -field AT_URLPROTOCOL

Indicates a protocol, such as <code>http</code> or <code>mailto</code>.


### -field AT_STARTMENUCLIENT

Indicates the owner of the startmenu client for a mail or Internet hyperlink. As of Windows 7, this value is used only for the MAPI sendmail client.


### -field AT_MIMETYPE

Indicates the MIME type, such as <code>audio/mp3</code>.

