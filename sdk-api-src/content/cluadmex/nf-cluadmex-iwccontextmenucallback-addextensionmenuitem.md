---
UID: NF:cluadmex.IWCContextMenuCallback.AddExtensionMenuItem
title: IWCContextMenuCallback::AddExtensionMenuItem (cluadmex.h)
description: Adds a menu item to a Failover Cluster Administrator context menu.
helpviewer_keywords: ["AddExtensionMenuItem","AddExtensionMenuItem method [Failover Cluster]","AddExtensionMenuItem method [Failover Cluster]","IWCContextMenuCallback interface","IWCContextMenuCallback interface [Failover Cluster]","AddExtensionMenuItem method","IWCContextMenuCallback.AddExtensionMenuItem","IWCContextMenuCallback::AddExtensionMenuItem","MF_CHECKED","MF_DISABLED","MF_ENABLED","MF_GRAYED","MF_MENUBARBREAK","MF_MENUBREAK","MF_SEPARATOR","MF_STRING","MF_UNCHECKED","_wolf_iwccontextmenucallback_addextensionmenuitem","cluadmex/IWCContextMenuCallback::AddExtensionMenuItem","mscs.iwccontextmenucallback_addextensionmenuitem"]
old-location: mscs\iwccontextmenucallback_addextensionmenuitem.htm
tech.root: MsCS
ms.assetid: 0eedc564-c82d-4309-b11c-c87d2e73c2c9
ms.date: 12/05/2018
ms.keywords: AddExtensionMenuItem, AddExtensionMenuItem method [Failover Cluster], AddExtensionMenuItem method [Failover Cluster],IWCContextMenuCallback interface, IWCContextMenuCallback interface [Failover Cluster],AddExtensionMenuItem method, IWCContextMenuCallback.AddExtensionMenuItem, IWCContextMenuCallback::AddExtensionMenuItem, MF_CHECKED, MF_DISABLED, MF_ENABLED, MF_GRAYED, MF_MENUBARBREAK, MF_MENUBREAK, MF_SEPARATOR, MF_STRING, MF_UNCHECKED, _wolf_iwccontextmenucallback_addextensionmenuitem, cluadmex/IWCContextMenuCallback::AddExtensionMenuItem, mscs.iwccontextmenucallback_addextensionmenuitem
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
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
 - IWCContextMenuCallback::AddExtensionMenuItem
 - cluadmex/IWCContextMenuCallback::AddExtensionMenuItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IWCContextMenuCallback.AddExtensionMenuItem
---

# IWCContextMenuCallback::AddExtensionMenuItem


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Adds a menu item to a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> context menu.

## -parameters

### -param lpszName [in]

Pointer to a null-terminated Unicode string containing the name of the item to be added to the menu. Although 
       declared as a <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.

### -param lpszStatusBarText [in]

Pointer to text to display on the status bar when the new item is selected. Although declared as a 
       <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.

### -param nCommandID [in]

Identifier for the command to be invoked when the menu item is selected. The 
       <i>nCommandID</i> parameter must not be set to –1.

### -param nSubmenuCommandID [in]

Identifier for a submenu. Submenus are not supported, and the <i>nSubmenuCommandID</i> 
       parameter must be zero.

### -param uFlags [in]

Bitmask of flags that describes the new menu item. One or more of the following values may be set.



#### MF_CHECKED (8)

Acts as a toggle with <b>MF_UNCHECKED</b> to place the default check mark next to the 
         item.



#### MF_UNCHECKED (0)

Acts as a toggle with <b>MF_CHECKED</b> to remove a check mark placed next to the 
         item.



#### MF_DISABLED (2)

Disables the menu item so it cannot be selected but does not dim it.



#### MF_ENABLED (0)

Enables the menu item so it can be selected and restores it from its dimmed state if the item was 
         previously dimmed.



#### MF_GRAYED (1)

Disables the menu item so it cannot be selected and dims it.



#### MF_MENUBARBREAK (32 (0x20))

Places the item in a new column. The new column is separated from the old column by a vertical dividing 
         line.



#### MF_MENUBREAK (64 (0x40))

Places the item in a new column. No dividing line is placed between the columns.



#### MF_SEPARATOR (2048 (0x800))

Draws a horizontal dividing line. This line cannot be dimmed, disabled, or highlighted. The 
         <i>lpszName</i> and <i>lpszStatusBarText</i> parameters are 
         ignored.



#### MF_STRING (0)

Specifies that the menu item is a character string. The <i>lpszName</i> parameter 
         contains a pointer to a <b>NULL</b>-terminated Unicode string. This is the default 
         interpretation.

## -returns

If <b>AddExtensionMenuItem</b> 
       is not successful, it can return other <b>HRESULT</b> values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
The <i>uFlags</i> parameter was set to either <b>MF_OWNERDRAW</b> 
         or <b>MF_POPUP</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000e</dt>
</dl>
</td>
<td width="60%">
There was an error allocating the menu item.

</td>
</tr>
</table>

## -remarks

The <b>AddExtensionMenuItem</b> 
     method adds items at the top of the context menu and follows them by a separator. The command identified by 
     <i>nCommandID</i> is passed in the <i>nCommandID</i> parameter to the 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a> method 
     when the user selects this menu item.

Note that the <b>MF_OWNERDRAW</b> and <b>MF_POPUP</b> flags are not 
     supported specifically for the <i>uFlags</i> parameter.


<a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extensions call 
     <b>AddExtensionMenuItem</b> from 
     their 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a> 
     method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwccontextmenucallback">IWCContextMenuCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>