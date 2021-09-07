---
UID: NF:propsys.IPropertyDescription.GetEditInvitation
title: IPropertyDescription::GetEditInvitation (propsys.h)
description: Gets the text used in edit controls hosted in various dialog boxes.
old-location: properties\IPropertyDescription_GetEditInvitation.htm
tech.root: properties
ms.assetid: 4b7ce948-6501-4220-aa44-e7422e70d9e5
ms.date: 12/05/2018
ms.keywords: GetEditInvitation, GetEditInvitation method [Windows Properties], GetEditInvitation method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetEditInvitation method, IPropertyDescription.GetEditInvitation, IPropertyDescription::GetEditInvitation, properties.IPropertyDescription_GetEditInvitation, propsys/IPropertyDescription::GetEditInvitation, shell.IPropertyDescription_GetEditInvitation, shell_IPropertyDescription_GetEditInvitation
req.header: propsys.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription::GetEditInvitation
 - propsys/IPropertyDescription::GetEditInvitation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - propsys.h
api_name:
 - IPropertyDescription.GetEditInvitation
---

# IPropertyDescription::GetEditInvitation


## -description

Gets the text used in edit controls hosted in various dialog boxes.

## -parameters

### -param ppszInvite [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode buffer that holds the invitation text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The information retrieved by this method comes from the <i>invitationText</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-labelinfo">labelInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the string referred to by <i>pszInvite</i> when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>