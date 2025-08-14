---
UID: NF:oleacc.AccessibleObjectFromEvent
title: AccessibleObjectFromEvent function (oleacc.h)
description: Retrieves the address of the IAccessible interface for the object that generated the event that is currently being processed by the client's event hook function.
helpviewer_keywords: ["AccessibleObjectFromEvent","AccessibleObjectFromEvent function [Windows Accessibility]","_msaa_AccessibleObjectFromEvent","msaa.accessibleobjectfromevent","oleacc/AccessibleObjectFromEvent","winauto.accessibleobjectfromevent"]
old-location: winauto\accessibleobjectfromevent.htm
tech.root: WinAuto
ms.assetid: d453c163-3918-4a1c-9636-16816227a295
ms.date: 12/05/2018
ms.keywords: AccessibleObjectFromEvent, AccessibleObjectFromEvent function [Windows Accessibility], _msaa_AccessibleObjectFromEvent, msaa.accessibleobjectfromevent, oleacc/AccessibleObjectFromEvent, winauto.accessibleobjectfromevent
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
 - AccessibleObjectFromEvent
 - oleacc/AccessibleObjectFromEvent
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
api_name:
 - AccessibleObjectFromEvent
---

# AccessibleObjectFromEvent function


## -description

Retrieves the address of the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface for the object that generated the event that is currently being processed by the client's event hook function.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Specifies the window handle of the window that generated the event. This value must be the window handle that is sent to the event hook function.

### -param dwId [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the object ID of the object that generated the event. This value must be the object ID that is sent to the event hook function.

### -param dwChildId [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies whether the event was triggered by an object or one of its child elements. If the object triggered the event, <i>dwChildID</i> is CHILDID_SELF. If a child element triggered the event, <i>dwChildID</i> is the element's child ID. This value must be the child ID that is sent to the event hook function.

### -param ppacc [out]

Type: <b>IAccessible**</b>

Address of a pointer variable that receives the address of an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface. The interface is either for the object that generated the event, or for the parent of the element that generated the event.

### -param pvarChild [out]

Type: <b>VARIANT*</b>

Address of a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a> that specifies the child ID that can be used to access information about the UI element.

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
</table>

## -remarks

Clients call this function within an event hook function to obtain an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer to either the object that generated the event or to the parent of the element that generated the event. The parameters sent to the <a href="/windows/desktop/api/winuser/nc-winuser-wineventproc">WinEventProc</a> callback function must be used for this function's <i>hwnd</i>, <i>dwObjectID</i>, and <i>dwChildID</i> parameters.

This function retrieves the lowest-level accessible object in the object hierarchy that is associated with an event. If the element that generated the event is not an accessible object (that is, does not support <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>), then the function retrieves the <b>IAccessible</b> interface of the parent object. The parent object must provide information about the child element through the <b>IAccessible</b> interface.

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.

This function fails if called in response to <a href="/windows/desktop/WinAuto/event-constants">EVENT_OBJECT_CREATE</a> because the object is not fully initialized. Similarly, clients should not call this in response to <a href="/windows/desktop/WinAuto/event-constants">EVENT_OBJECT_DESTROY</a> because the object is no longer available and cannot respond. Clients watch for <a href="/windows/desktop/WinAuto/event-constants">EVENT_OBJECT_SHOW</a> and <a href="/windows/desktop/WinAuto/event-constants">EVENT_OBJECT_HIDE</a> events rather than for <b>EVENT_OBJECT_CREATE</b> and <b>EVENT_OBJECT_DESTROY</b>.


#### Examples

The following example code shows this method being called in a <a href="/windows/desktop/api/winuser/nc-winuser-wineventproc">WinEventProc</a> event handler.




```

void CALLBACK HandleWinEvent(HWINEVENTHOOK hook, DWORD event, HWND hwnd, 
                             LONG idObject, LONG idChild, 
                             DWORD dwEventThread, DWORD dwmsEventTime)
{
    IAccessible* pAcc = NULL;
    VARIANT varChild;
    HRESULT hr = AccessibleObjectFromEvent(hwnd, idObject, idChild, &pAcc, &varChild);  
    if ((hr == S_OK) && (pAcc != NULL))
    {
        // Do something with the accessible object, then release it.        
        // ... 
        pAcc->Release();
    }
}

```

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-accessibleobjectfrompoint">AccessibleObjectFromPoint</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-accessibleobjectfromwindow">AccessibleObjectFromWindow</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>



<a href="/windows/desktop/api/winuser/nc-winuser-wineventproc">WinEventProc</a>