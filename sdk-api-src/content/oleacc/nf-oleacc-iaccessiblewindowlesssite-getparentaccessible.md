---
UID: NF:oleacc.IAccessibleWindowlessSite.GetParentAccessible
title: IAccessibleWindowlessSite::GetParentAccessible
author: windows-sdk-content
description: Retrieves an IAccessible pointer for the parent of a windowless Microsoft ActiveX control in the accessibility tree.
old-location: winauto\uiauto_IAccessibleWindowlessSite_GetParentAccessible.htm
tech.root: WinAuto
ms.assetid: 579C2425-9C3E-4CFF-8A25-C661670FB636
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetParentAccessible, GetParentAccessible method [Windows Accessibility], GetParentAccessible method [Windows Accessibility],IAccessibleWindowlessSite interface, IAccessibleWindowlessSite interface [Windows Accessibility],GetParentAccessible method, IAccessibleWindowlessSite.GetParentAccessible, IAccessibleWindowlessSite::GetParentAccessible, oleacc/IAccessibleWindowlessSite::GetParentAccessible, winauto.uiauto_IAccessibleWindowlessSite_GetParentAccessible
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessibleWindowlessSite.GetParentAccessible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibleWindowlessSite::GetParentAccessible


## -description


Retrieves an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> pointer for the parent of a windowless Microsoft ActiveX control in the accessibility tree.


## -parameters




### -param ppParent [out, optional]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>**</b>

Receives the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> pointer for the parent of the windowless ActiveX control.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To return its parent <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object, an object that implements <b>IAccessible</b> must be able to implement the <a href="https://msdn.microsoft.com/7c8c5208-ea77-47b2-913d-314ade0313f5">get_accParent</a> method.  Implementing <b>get_accParent</b> is difficult for a   windowless  ActiveX control because the control might be unable to determine its location in the accessible tree of the parent object.  The <b>GetParentAccessible</b> method enables a windowless ActiveX control to query its site for the parent object, and then return the parent object to the client that called <b>get_accParent</b>.




## -see-also




<a href="https://msdn.microsoft.com/1ED23B39-231B-46A2-9FED-969A36DA8DD9">IAccessibleWindowlessSite</a>
 

 

