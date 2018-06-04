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

# SHCreateShellItem function


## -description


Creates an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object.
        
            
<div class="alert"><b>Note</b>  It is recommended that you use <a href="https://msdn.microsoft.com/8fb84a20-d8f2-4c7c-bfb1-a22791b8636a">SHCreateItemWithParent</a> or <a href="https://msdn.microsoft.com/a6dcddd9-cdbc-4cf9-97e3-d1b562283344">SHCreateItemFromIDList</a> instead of this function.</div><div> </div>

## -parameters




### -param pidlParent [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL to the parent. This value can be <b>NULL</b>.


### -param psfParent [in, optional]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the parent <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>. This value can be <b>NULL</b>.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL to the requested item. If parent information is not included in <i>pidlParent</i> or <i>psfParent</i>, this must be an absolute PIDL.


### -param ppsi [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When this method returns, contains the interface pointer to the new <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SHCreateShellItem</b> creates an object that represents a Shell namespace item. The caller must provide parent information in <i>pidlParent</i> or <i>psfParent</i>; alternatively, the caller can provide an absolute IDList in the <i>pidl</i> parameter.

There are three valid calling patterns for this function:

                

<ol>
<li>The parent folder is identified by an absolute IDList <i>pidlParent</i>. The <i>pidl</i> parameter points to a child IDList that identifies the item within the folder identified by <i>pidlParent</i>.

                        <div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IShellItem *psi;
SHCreateShellItem(pidlParent, NULL, pidlChild, &amp;psi);
</pre>
</td>
</tr>
</table></span></div>
</li>
<li>The parent folder is identified by <i>psfParent</i>. The <i>pidl</i> parameter points to a child IDList that identifies the item within the folder identified by <i>psfParent</i>.

                        <div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IShellItem *psi;
SHCreateShellItem(NULL, psfParent, pidlChild, &amp;psi);
</pre>
</td>
</tr>
</table></span></div>
</li>
<li>The item is identified by an absolute IDList passed to the <i>pidl</i> parameter.

                        <div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IShellItem *psi;
SHCreateShellItem(NULL, NULL, pidlFull, &amp;psi);
</pre>
</td>
</tr>
</table></span></div>
</li>
</ol>


