---
UID: NE:shobjidl_core.ASSOCIATIONTYPE
title: ASSOCIATIONTYPE
author: windows-sdk-content
description: Specifies the type of association for an application. Used by methods of the IApplicationAssociationRegistration interface.
old-location: shell\ASSOCIATIONTYPE.htm
old-project: shell
ms.assetid: 3dbbe748-5e83-4103-932a-b51a2a55f9fd
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: ASSOCIATIONTYPE, ASSOCIATIONTYPE enumeration [Windows Shell], AT_FILEEXTENSION, AT_MIMETYPE, AT_STARTMENUCLIENT, AT_URLPROTOCOL, _shell_ASSOCIATIONTYPE, shell.ASSOCIATIONTYPE, shobjidl_core/ASSOCIATIONTYPE, shobjidl_core/AT_FILEEXTENSION, shobjidl_core/AT_MIMETYPE, shobjidl_core/AT_STARTMENUCLIENT, shobjidl_core/AT_URLPROTOCOL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ASSOCIATIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - ASSOCIATIONTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
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

