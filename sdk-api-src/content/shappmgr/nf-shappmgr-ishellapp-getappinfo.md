---
UID: NF:shappmgr.IShellApp.GetAppInfo
title: IShellApp::GetAppInfo
author: windows-driver-content
description: Gets general information about an application.
old-location: shell\IShellApp_GetAppInfo.htm
old-project: shell
ms.assetid: 8842c12e-2b59-49d6-8140-5a402509a0dd
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetAppInfo, GetAppInfo method [Windows Shell], GetAppInfo method [Windows Shell],IShellApp interface, IShellApp interface [Windows Shell],GetAppInfo method, IShellApp.GetAppInfo, IShellApp::GetAppInfo, inet_IShellApp_GetAppInfo, shappmgr/IShellApp::GetAppInfo, shell.IShellApp_GetAppInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellApp.GetAppInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IShellApp::GetAppInfo


## -description



		Gets general information about an application.
		


## -parameters




### -param pai






#### - pInfo [out]

Type: <b><a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">APPINFODATA</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">APPINFODATA</a> structure that returns the application information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Add/Remove Programs in the Control Panel sets the cbSize and dwMask members of the <a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">APPINFODATA</a> structure.</div>
<div> </div>
  Your implementation should validate cbSize by comparing it with the size of <a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">APPINFODATA</a>.  If cbSize does not equal the size of <b>APPINFODATA</b>, this method should return a COM error value like E_FAIL.

Add/Remove Programs in the Control Panel will set the dwMask member of the <a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">APPINFODATA</a> structure to indicate that you should return AIM_DISPLAYNAME and AIM_SUPPORTURL. For each value that you return in APPINFODATA, you must set the corresponding bit in dwMask.  All other bits should be cleared.
			


#### Examples

Here is a sample of how to use the dwMask bits::

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CPubApp::GetAppInfo(APPINFODATA *pData)
{
    if (sizeof(APPINFODATA) != pData-&gt;cbSize)
        return E_FAIL;

    // First save off the mask of requested data items.

    const DWORD dwMask = pData-&gt;dwMask;

    // Zero-out the mask.  Bits will be set as items are obtained. 

    pData-&gt;dwMask = 0;

    // Call an internal function that obtains data and sets
    // bits in pData-&gt;dwMask for each item obtained.

    return get_app_info_data(pData, dwMask);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">APPINFODATA</a>



<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>



<a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>
 

 

