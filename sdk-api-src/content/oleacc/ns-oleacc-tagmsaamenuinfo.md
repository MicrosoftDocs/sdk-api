---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

The <b>MSAAMENUINFO</b> structure is the first member of the application-specific structure (or class) that contains the data for an owner-drawn menu item, which is pointed to by the <b>dwItemData</b> member of the <a href="winui._win32_MENUITEMINFO_str">MENUITEMINFO</a> structure.

The <b>MSAAMENUINFO</b> structure cannot be a member in a class that contains virtual functions because the first member of the class is always a compiler-generated pointer to a table of the virtual functions. To work around this problem, you can implement a structure that contains the <b>MSAAMENUINFO</b> as the first member, and a pointer to the class with the virtual functions as a second member, which contains the owner-drawn item data.


#### Examples

The following code fragment shows the declaration of an application-specific owner-drawn menu information structure that includes <b>MSAAMENUINFO</b>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/93b51cbb-b7b4-4a38-ba69-d6345a269944">Exposing Owner-Drawn Menu Items</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>
 

 

