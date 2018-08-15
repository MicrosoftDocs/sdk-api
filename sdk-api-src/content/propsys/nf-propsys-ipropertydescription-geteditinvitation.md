---
UID: NF:propsys.IPropertyDescription.GetEditInvitation
title: IPropertyDescription::GetEditInvitation
author: windows-sdk-content
description: Gets the text used in edit controls hosted in various dialog boxes.
old-location: properties\IPropertyDescription_GetEditInvitation.htm
old-project: properties
ms.assetid: 4b7ce948-6501-4220-aa44-e7422e70d9e5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetEditInvitation, GetEditInvitation method [Windows Properties], GetEditInvitation method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetEditInvitation method, IPropertyDescription.GetEditInvitation, IPropertyDescription::GetEditInvitation, properties.IPropertyDescription_GetEditInvitation, propsys/IPropertyDescription::GetEditInvitation, shell.IPropertyDescription_GetEditInvitation, shell_IPropertyDescription_GetEditInvitation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: Shobjidl.h
req.redist: 
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
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - propsys.h
api_name:
 - IPropertyDescription.GetEditInvitation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetEditInvitation


## -description


Gets the text used in edit controls hosted in various dialog boxes.


## -parameters




### -param ppszInvite






#### - pszInvite [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode buffer that holds the invitation text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The information retrieved by this method comes from the <i>invitationText</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773876(v=VS.85).aspx">labelInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the string referred to by <i>pszInvite</i> when it is no longer needed.
            




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

