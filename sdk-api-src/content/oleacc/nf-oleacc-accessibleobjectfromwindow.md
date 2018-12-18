---
UID: NF:oleacc.AccessibleObjectFromWindow
title: AccessibleObjectFromWindow function
author: windows-sdk-content
description: Retrieves the address of the specified interface for the object associated with the specified window.
old-location: winauto\accessibleobjectfromwindow.htm
tech.root: WinAuto
ms.assetid: 297ac50f-2a58-477b-ba57-5d1416c191b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AccessibleObjectFromWindow, AccessibleObjectFromWindow function [Windows Accessibility], _msaa_AccessibleObjectFromWindow, msaa.accessibleobjectfromwindow, oleacc/AccessibleObjectFromWindow, winauto.accessibleobjectfromwindow
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
 - Ext-MS-Win-oleacc-l1-1-0.dll
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - AccessibleObjectFromWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# AccessibleObjectFromWindow function


## -description


Retrieves the address of the specified interface for the object associated with the specified window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Specifies the handle of a window for which an object is to be retrieved. To retrieve an interface pointer to the cursor or caret object, specify <b>NULL</b> and use the appropriate object ID in <i>dwObjectID</i>.


### -param dwId [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the object ID. This value is one of the standard <a href="https://msdn.microsoft.com/dc1603f8-29e5-4acd-817a-c6957feaff6c">object identifier</a> constants or a custom object ID such as <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_NATIVEOM</a>, which is the object ID for the Office native object model. For more information about <b>OBJID_NATIVEOM</b>, see the Remarks section in this topic.


### -param riid [in]

Type: <b>REFIID</b>

Specifies the reference identifier of the requested interface. This value is either IID_IAccessible or IID_IDispatch, but it can also be IID_IUnknown, or the IID of any interface that the object is expected to support.


### -param ppvObject [out]

Type: <b>void**</b>

Address of a pointer variable that receives the address of the specified interface.


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns one of the following or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.

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



Clients call this function to retrieve the address of an object's <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>, <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>, <a href="https://go.microsoft.com/fwlink/p/?linkid=120799">IEnumVARIANT</a>, <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, or other supported interface pointer.

As with other <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="https://msdn.microsoft.com/408bfa47-fda0-4a25-89c1-da41d967ad61">Receiving Errors for IAccessible Interface Pointers</a>.

Clients use this function to obtain access to the Microsoft Office 2000 native object model. The native object model provides clients with accessibility information about an Office application's document or client area that is not exposed by Microsoft Active Accessibility.

To obtain an <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface pointer to a class supported by the native object model, specify <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_NATIVEOM</a> in <i>dwObjectID</i>. When using this object identifier, the <i>hwnd</i> parameter must match the following window class types.

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
 

Note that the above window classes correspond to the innermost document window or pane window. For more information about the Office object model, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=186469">Microsoft Office 2000/Visual Basic Programmer's Guide</a>.




## -see-also




<a href="https://msdn.microsoft.com/d453c163-3918-4a1c-9636-16816227a295">AccessibleObjectFromEvent</a>



<a href="https://msdn.microsoft.com/b781b74f-5c36-4a65-a9b1-ecf7f8e5b531">AccessibleObjectFromPoint</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>
 

 

