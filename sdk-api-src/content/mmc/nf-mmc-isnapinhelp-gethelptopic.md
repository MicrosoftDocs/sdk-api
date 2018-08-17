---
UID: NF:mmc.ISnapinHelp.GetHelpTopic
title: ISnapinHelp::GetHelpTopic
author: windows-sdk-content
description: Enables a snap-in to add its compiled HTML Help file to the MMC Help collection file.
old-location: mmc\isnapinhelp_gethelptopic.htm
old-project: mmc
ms.assetid: 2F7E987F-1E1E-4C9E-9B26-D7BB8F5A05DD
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetHelpTopic, GetHelpTopic method [MMC], GetHelpTopic method [MMC],ISnapinHelp interface, ISnapinHelp interface [MMC],GetHelpTopic method, ISnapinHelp.GetHelpTopic, ISnapinHelp::GetHelpTopic, mmc.isnapinhelp_gethelptopic, mmc/ISnapinHelp::GetHelpTopic
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinHelp.GetHelpTopic
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinHelp::GetHelpTopic


## -description


Enables a snap-in to add its compiled HTML Help file to the MMC Help collection file.


## -parameters




### -param lpCompiledHelpFile [out]

A pointer to the address of the null-terminated Unicode string that contains the path of the compiled Help file (.chm) for the snap-in. When specifying the path, place the file anywhere and specify the full path name.


## -returns



This method can return one of these values.




## -remarks



MMC calls the snap-in's implementation of this method to get the location of the snap-in's Help file. MMC merges the HTML Help files of all snap-ins with the MMC console HTML Help collection file.

The topic hierarchy from the snap-in's Help file will appear in the table of contents when the collection is viewed.

By merging the HTML Help files, MMC creates a single, integrated HTML Help table of contents, index, and search feature. When a user clicks Help on Microsoft Management Console on the main 
<b>Help</b> menu, MMC opens the merged Help file that includes HTML Help files for all snap-ins in the current console file.

Allocate the <i>lpCompiledHelpFile</i> string with the COM API function <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CComponentData::GetHelpTopic( LPOLESTR *lpCompiledFile )
{
    LPOLESTR lpHelpFile;
 
    if ( !lpCompiledFile )
        return E_POINTER; // invalid argument
 
    lpHelpFile = (LPOLESTR) CoTaskMemAlloc( MAX_PATH * sizeof(WCHAR) );
 
    if ( !lpHelpFile )
    {
        return E_OUTOFMEMORY;
    }
 
    ExpandEnvironmentStringsW( L"%SystemRoot%\\Help\\myhelpfile.chm", lpHelpFile, MAX_PATH );
 
    *lpCompiledHelpFile = lpHelpFile;
 
    return S_OK;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/87387cf5-ff5f-4816-8c96-97a7ae25df94">Adding HTML Help Support</a>



<a href="https://msdn.microsoft.com/184adc09-8b48-4a2e-bbd9-ec6bd9085c32">IDisplayHelp::ShowTopic</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt300864(v=VS.85).aspx">ISnapinHelp</a>



<a href="https://msdn.microsoft.com/c3b0fa86-dff4-4c35-9b08-633448db18be">MMCPropertyHelp</a>



<a href="https://msdn.microsoft.com/01a13430-e64e-4e3a-8db9-1d42ad9b32bb">Providing MUI-Compliant Help Files</a>
 

 

