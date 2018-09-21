---
UID: NS:oleacc.tagMSAAMENUINFO
title: tagMSAAMENUINFO
author: windows-sdk-content
description: Used by server developers to expose the names of owner-drawn menu items.
old-location: winauto\msaamenuinfo.htm
tech.root: WinAuto
ms.assetid: e8cc9c5d-eb76-4dba-90ad-94d2fd86dc8b
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*LPMSAAMENUINFO, LPMSAAMENUINFO, LPMSAAMENUINFO structure pointer [Windows Accessibility], MSAAMENUINFO, MSAAMENUINFO structure [Windows Accessibility], _msaa_MSAAMENUINFO, msaa.msaamenuinfo, oleacc/LPMSAAMENUINFO, oleacc/MSAAMENUINFO, tagMSAAMENUINFO, winauto.msaamenuinfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Oleacc.h
api_name:
 - MSAAMENUINFO
product: Windows
targetos: Windows
req.typenames: MSAAMENUINFO, *LPMSAAMENUINFO
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# tagMSAAMENUINFO structure


## -description



Used by server developers to expose the names of owner-drawn menu items.




## -struct-fields




### -field dwMSAASignature

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Must be MSAA_MENU_SIG, which is defined in oleacc.h.


### -field cchWText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Length, in characters, of the text for the menu item, <b>not including</b> the Unicode null-terminated character.


### -field pszWText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

The text of the menu item, in Unicode, <b>including</b> the Unicode null-terminated character.


## -remarks



By associating the <b>MSAAMENUINFO</b> structure with owner-drawn menu item data, server developers can expose the menu items without having to implement <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>.

The <b>MSAAMENUINFO</b> structure is the first member of the application-specific structure (or class) that contains the data for an owner-drawn menu item, which is pointed to by the <b>dwItemData</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms647578(v=VS.85).aspx">MENUITEMINFO</a> structure.

The <b>MSAAMENUINFO</b> structure cannot be a member in a class that contains virtual functions because the first member of the class is always a compiler-generated pointer to a table of the virtual functions. To work around this problem, you can implement a structure that contains the <b>MSAAMENUINFO</b> as the first member, and a pointer to the class with the virtual functions as a second member, which contains the owner-drawn item data.


#### Examples

The following code fragment shows the declaration of an application-specific owner-drawn menu information structure that includes <b>MSAAMENUINFO</b>:


```

// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these. MSAAMENUINFO must be the first 
// member. 
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first element.
    LPTSTR       m_pName;      // Menu text, for display. NULL for
                               //  separator item.
    int          m_CmdID;      // Menu command ID.
    int          m_IconIndex;  // Index of icon in bitmap.
};

```





## -see-also




<a href="https://msdn.microsoft.com/93b51cbb-b7b4-4a38-ba69-d6345a269944">Exposing Owner-Drawn Menu Items</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>
 

 

