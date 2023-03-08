---
UID: NF:uiautomationclient.IUIAutomation.RectToVariant
title: IUIAutomation::RectToVariant (uiautomationclient.h)
description: Creates a VARIANT that contains the coordinates of a rectangle.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","RectToVariant method","IUIAutomation.RectToVariant","IUIAutomation::RectToVariant","RectToVariant","RectToVariant method [Windows Accessibility]","RectToVariant method [Windows Accessibility]","IUIAutomation interface","uiauto.uiauto_IUIAutomation_RectToVariant","uiauto_IUIAutomation_RectToVariant","uiautomationclient/IUIAutomation::RectToVariant","winauto.uiauto_IUIAutomation_RectToVariant"]
old-location: winauto\uiauto_IUIAutomation_RectToVariant.htm
tech.root: WinAuto
ms.assetid: abfb2bb1-7594-4f32-9188-05745006ae18
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],RectToVariant method, IUIAutomation.RectToVariant, IUIAutomation::RectToVariant, RectToVariant, RectToVariant method [Windows Accessibility], RectToVariant method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_RectToVariant, uiauto_IUIAutomation_RectToVariant, uiautomationclient/IUIAutomation::RectToVariant, winauto.uiauto_IUIAutomation_RectToVariant
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomation::RectToVariant
 - uiautomationclient/IUIAutomation::RectToVariant
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.RectToVariant
---

# IUIAutomation::RectToVariant


## -description

Creates a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> that contains the coordinates of a rectangle.

## -parameters

### -param rc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a structure that contains the coordinates of the rectangle.

### -param var [out, retval]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>*</b>

Receives the coordinates of the rectangle.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The returned <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> has a data type of VT_ARRAY | VT_R8.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-varianttorect">IUIAutomation::VariantToRect</a>