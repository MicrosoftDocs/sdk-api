---
UID: NF:propsys.IPropertyDescriptionList.GetAt
title: IPropertyDescriptionList::GetAt (propsys.h)
author: windows-sdk-content
description: Gets the property description at the specified index in a property description list.
old-location: properties\IPropertyDescriptionList_GetAt.htm
tech.root: properties
ms.assetid: ab4967b8-6650-49fa-b6d5-d72688b080db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [Windows Properties], GetAt method [Windows Properties],IPropertyDescriptionList interface, IPropertyDescriptionList interface [Windows Properties],GetAt method, IPropertyDescriptionList.GetAt, IPropertyDescriptionList::GetAt, _shell_IPropertyDescriptionList_GetAt, properties.IPropertyDescriptionList_GetAt, propsys/IPropertyDescriptionList::GetAt, shell.IPropertyDescriptionList_GetAt
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionList.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescriptionList::GetAt


## -description


Gets the property description at the specified index in a property description list.


## -parameters




### -param iElem [in]

Type: <b>UINT</b>

The number of the property in the list string.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the requested property description interface, typically IID_IPropertyDescription.
        


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. Typically, this is <a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that you use the IID_PPV_ARGS macro, defined in objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, eliminating the possibility of a coding error.
      



