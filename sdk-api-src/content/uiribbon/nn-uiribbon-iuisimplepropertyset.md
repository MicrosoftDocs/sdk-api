---
UID: NN:uiribbon.IUISimplePropertySet
title: IUISimplePropertySet (uiribbon.h)
description: IUISimplePropertySet is a read-only interface that defines a method for retrieving the value identified by a property key.
helpviewer_keywords: ["IUISimplePropertySet","IUISimplePropertySet interface [Windows Ribbon]","IUISimplePropertySet interface [Windows Ribbon]","described","scenicintent_IUISimplePropertySet","uiribbon/IUISimplePropertySet","windowsribbon.windowsribbon_iuisimplepropertyset"]
old-location: windowsribbon\windowsribbon_iuisimplepropertyset.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuisimplepropertyset\iuisimplepropertyset.htm
ms.date: 12/05/2018
ms.keywords: IUISimplePropertySet, IUISimplePropertySet interface [Windows Ribbon], IUISimplePropertySet interface [Windows Ribbon],described, scenicintent_IUISimplePropertySet, uiribbon/IUISimplePropertySet, windowsribbon.windowsribbon_iuisimplepropertyset
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUISimplePropertySet
 - uiribbon/IUISimplePropertySet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUISimplePropertySet
---

# IUISimplePropertySet interface


## -description

<b>IUISimplePropertySet</b> is a read-only interface that defines a method for retrieving the value identified by a  property key. This interface is implemented by the Windows Ribbon framework and is also implemented by  the host application for each item in the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a> object of an item gallery.

When implemented by the host application, the method defined by this interface is used to retrieve a property key  value for the selected item in the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

## -inheritance

The <b>IUISimplePropertySet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUISimplePropertySet</b> also has these types of members:

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties">Property Keys</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>



<a href="/windows/desktop/windowsribbon/ribbon-controls-galleries">Working with Galleries</a>
