---
UID: NF:oleacc.IAccessibleHandler.AccessibleObjectFromID
title: IAccessibleHandler::AccessibleObjectFromID (oleacc.h)
description: The AccessibleObjectFromID method retrieves an IAccessibleinterface pointer for the interface associated with the given object ID. Oleacc.dll uses this method to obtain an IAccessible interface pointer for proxies that are supplied by other code.
helpviewer_keywords: ["AccessibleObjectFromID","AccessibleObjectFromID method [Windows Accessibility]","AccessibleObjectFromID method [Windows Accessibility]","IAccessibleHandler interface","IAccessibleHandler interface [Windows Accessibility]","AccessibleObjectFromID method","IAccessibleHandler.AccessibleObjectFromID","IAccessibleHandler::AccessibleObjectFromID","_msaa_IAccessibleHandler_AccessibleObjectFromID","msaa.iaccessiblehandler_iaccessiblehandler__accessibleobjectfromid","oleacc/IAccessibleHandler::AccessibleObjectFromID","winauto.iaccessiblehandler_iaccessiblehandler__accessibleobjectfromid"]
old-location: winauto\iaccessiblehandler_iaccessiblehandler__accessibleobjectfromid.htm
tech.root: WinAuto
ms.assetid: c552b26a-a8db-42a1-85c9-9578230def74
ms.date: 12/05/2018
ms.keywords: AccessibleObjectFromID, AccessibleObjectFromID method [Windows Accessibility], AccessibleObjectFromID method [Windows Accessibility],IAccessibleHandler interface, IAccessibleHandler interface [Windows Accessibility],AccessibleObjectFromID method, IAccessibleHandler.AccessibleObjectFromID, IAccessibleHandler::AccessibleObjectFromID, _msaa_IAccessibleHandler_AccessibleObjectFromID, msaa.iaccessiblehandler_iaccessiblehandler__accessibleobjectfromid, oleacc/IAccessibleHandler::AccessibleObjectFromID, winauto.iaccessiblehandler_iaccessiblehandler__accessibleobjectfromid
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - IAccessibleHandler::AccessibleObjectFromID
 - oleacc/IAccessibleHandler::AccessibleObjectFromID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessibleHandler.AccessibleObjectFromID
---

# IAccessibleHandler::AccessibleObjectFromID


## -description

The <b>AccessibleObjectFromID</b> method retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer for the interface associated with the given object ID. Oleacc.dll uses this method to obtain an <b>IAccessible</b> interface pointer for proxies that are supplied by other code.
<div class="alert"><b>Note</b>  <b>IAccessibleHandler::AccessibleObjectFromID</b> is deprecated and should not be used.</div><div> </div>

## -parameters

### -param hwnd [in]

Type: <b>long</b>

Specifies the handle of a window for which an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer is to be retrieved.

### -param lObjectID [in]

Type: <b>long</b>

Specifies the object ID. This value is one of the standard <a href="/windows/desktop/WinAuto/object-identifiers">object identifier</a> constants or a custom object ID.

### -param pIAccessible [out]

Type: <b>LPACCESSIBLE*</b>

Specifies the address of a pointer variable that receives the address of the object's <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the following or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not supported.

</td>
</tr>
</table>

## -remarks

Oleacc calls this function to obtain an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer for <b>HWND</b>s that have the class name that this handler is registered for.

At startup, Oleacc looks in the registry key HKLM\SOFTWARE\Microsoft\Active Accessibility\Handlers and enumerates over each subkey (Oleacc expects the subkey to be a GUID). Oleacc reads the associated class name from HKCR\CLSID\{guid}\AccClassName, where {guid} was the GUID found under the HKLM\SOFTWARE\Microsoft\Active Accessibility\Handlers key. When Oleacc finds a window with a class name that matches the GUID, it CoCreates the object using the GUID, retrieves the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler">IAccessibleHandler</a> interface pointer, and calls <b>AccessibleObjectFromID</b> on it to get at <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer.

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.