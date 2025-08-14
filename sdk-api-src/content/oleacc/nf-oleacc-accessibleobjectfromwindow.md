---
UID: NF:oleacc.AccessibleObjectFromWindow
title: AccessibleObjectFromWindow function (oleacc.h)
description: Retrieves the address of the specified interface for the object associated with the specified window.
helpviewer_keywords: ["AccessibleObjectFromWindow","AccessibleObjectFromWindow function [Windows Accessibility]","_msaa_AccessibleObjectFromWindow","msaa.accessibleobjectfromwindow","oleacc/AccessibleObjectFromWindow","winauto.accessibleobjectfromwindow"]
old-location: winauto\accessibleobjectfromwindow.htm
tech.root: WinAuto
ms.assetid: 297ac50f-2a58-477b-ba57-5d1416c191b3
ms.date: 12/05/2018
ms.keywords: AccessibleObjectFromWindow, AccessibleObjectFromWindow function [Windows Accessibility], _msaa_AccessibleObjectFromWindow, msaa.accessibleobjectfromwindow, oleacc/AccessibleObjectFromWindow, winauto.accessibleobjectfromwindow
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
 - AccessibleObjectFromWindow
 - oleacc/AccessibleObjectFromWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-oleacc-l1-1-2.dll
 - Oleacc.dll
 - Ext-MS-Win-oleacc-l1-1-0.dll
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - AccessibleObjectFromWindow
---

# AccessibleObjectFromWindow function


## -description

Retrieves the address of the specified interface for the object associated with the specified window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Specifies the handle of a window for which an object is to be retrieved. To retrieve an interface pointer to the cursor or caret object, specify <b>NULL</b> and use the appropriate object ID in <i>dwObjectID</i>.

### -param dwId [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the object ID. This value is one of the standard <a href="/windows/desktop/WinAuto/object-identifiers">object identifier</a> constants or a custom object ID such as <a href="/windows/desktop/WinAuto/object-identifiers">OBJID_NATIVEOM</a>, which is the object ID for the Office native object model. For more information about <b>OBJID_NATIVEOM</b>, see the Remarks section in this topic.

### -param riid [in]

Type: <b>REFIID</b>

Specifies the reference identifier of the requested interface. This value is either IID_IAccessible or IID_IDispatch, but it can also be IID_IUnknown, or the IID of any interface that the object is expected to support.

### -param ppvObject [out]

Type: <b>void**</b>

Address of a pointer variable that receives the address of the specified interface.

## -returns

Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns one of the following or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

<table>
<tr>
<th>Return code</th>
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

Clients call this function to retrieve the address of an object's <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>, <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>, <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>, <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or other supported interface pointer.

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.

Clients use this function to obtain access to the Microsoft Office 2000 native object model. The native object model provides clients with accessibility information about an Office application's document or client area that is not exposed by Microsoft Active Accessibility.

To obtain an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface pointer to a class supported by the native object model, specify <a href="/windows/desktop/WinAuto/object-identifiers">OBJID_NATIVEOM</a> in <i>dwObjectID</i>. When using this object identifier, the <i>hwnd</i> parameter must match the following window class types.

<table>
<tr>
<th>Office application</th>
<th>Window class</th>
<th>IDispatch pointer to</th>
</tr>
<tr>
<td>Word</td>
<td>_WwG</td>
<td>Window</td>
</tr>
<tr>
<td>Excel</td>
<td>EXCEL7</td>
<td>Window</td>
</tr>
<tr>
<td>PowerPoint</td>
<td>paneClassDC</td>
<td>DocumentWindow</td>
</tr>
<tr>
<td>Command Bars</td>
<td>MsoCommandBar</td>
<td>CommandBar</td>
</tr>
</table>
 

Note that the above window classes correspond to the innermost document window or pane window. For more information about the Office object model, see the <a href="/previous-versions/office/developer/office2000/aa141393(v=office.10)">Microsoft Office 2000/Visual Basic Programmer's Guide</a>.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-accessibleobjectfromevent">AccessibleObjectFromEvent</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-accessibleobjectfrompoint">AccessibleObjectFromPoint</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>