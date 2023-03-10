---
UID: NN:propsys.IPropertyDescriptionList
title: IPropertyDescriptionList (propsys.h)
description: Exposes methods that extract information from a collection of property descriptions presented as a list.
helpviewer_keywords: ["IPropertyDescriptionList","IPropertyDescriptionList interface [Windows Properties]","IPropertyDescriptionList interface [Windows Properties]","described","_shell_IPropertyDescriptionList","properties.IPropertyDescriptionList","propsys/IPropertyDescriptionList","shell.IPropertyDescriptionList"]
old-location: properties\IPropertyDescriptionList.htm
tech.root: properties
ms.assetid: e0530195-27da-4df7-884f-518e905f3c0e
ms.date: 12/05/2018
ms.keywords: IPropertyDescriptionList, IPropertyDescriptionList interface [Windows Properties], IPropertyDescriptionList interface [Windows Properties],described, _shell_IPropertyDescriptionList, properties.IPropertyDescriptionList, propsys/IPropertyDescriptionList, shell.IPropertyDescriptionList
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyDescriptionList
 - propsys/IPropertyDescriptionList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionList
---

# IPropertyDescriptionList interface


## -description

Exposes methods that extract information from a collection of property descriptions presented as a list.

## -inheritance

The <b>IPropertyDescriptionList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyDescriptionList</b> also has these types of members:

## -remarks

Ordered lists of properties are used to select which properties are shown in various UI locations such as the details pane or an infotip.  The IPropertyDescriptionList interface provides access to the individual properties in such a list.  



To get an instance of the subsystem object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>, obtain an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a> interface and call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertydescriptionlist">IShellItem2::GetPropertyDescriptionList</a>, or obtain the list in string form and call <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a>. 

To obtain a property description list in string form, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getstring">IShellItem2::GetString</a> with one of the PKEY_PropList keys.  For example, <code>PKEY_PropList_InfoTip</code> (<a href="/windows/desktop/properties/props-system-proplist-infotip">System.PropList.InfoTip</a>) will return the string form of a list of properties suitable for showing in an infotip.  If you are reading multiple values from an item, it is more efficient to call <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getvalue">IPropertyStore::GetValue</a> with a PKEY_PropList key so that the item is not reopened multiple times.  See Property Lists for details on how to register a property list string for a file type.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a>
