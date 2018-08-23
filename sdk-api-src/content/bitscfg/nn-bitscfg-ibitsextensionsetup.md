---
UID: NN:bitscfg.IBITSExtensionSetup
title: IBITSExtensionSetup
author: windows-sdk-content
description: Use the IBITSExtensionSetup interface to enable or disable BITS uploads to a virtual directory.
old-location: bits\ibitsextensionsetup.htm
old-project: bits
ms.assetid: 840608ef-9c07-43f7-9cfd-20996a18bb50
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBITSExtensionSetup, IBITSExtensionSetup interface [BITS], IBITSExtensionSetup interface [BITS],described, _drz_ibitsextensionsetup, bits.ibitsextensionsetup, bitscfg/IBITSExtensionSetup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bitscfg.h
req.include-header: 
req.redist: BITS 1.5 on Windows XP
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bitscfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITS_FILE_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup
product: Windows
targetos: Windows
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
---

# IBITSExtensionSetup interface


## -description


Use the 
<b>IBITSExtensionSetup</b> interface to enable or disable BITS uploads to a virtual directory.

This interface is an ADSI extension. To get a pointer to this interface, call the 
<a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a> ADSI function as shown in Example Code.

If you use this interface from a setup program that also installs the BITS server, you must call the 
<a href="https://msdn.microsoft.com/ac0bb9d5-3f1f-4c9b-bd7d-905e0451bf70">IBITSExtensionSetupFactory::GetObject</a> method to get a pointer to this interface instead of calling the <a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBITSExtensionSetup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBITSExtensionSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBITSExtensionSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d439054-a751-4f63-9e82-223d1ce9c551">DisableBITSUploads</a>
</td>
<td align="left" width="63%">
Disables BITS uploads on the virtual directory to which the ADSI object points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b68dea2-f9a7-4a99-93d3-62c4f24b769f">EnableBITSUploads</a>
</td>
<td align="left" width="63%">
Enables BITS uploads on the virtual directory to which the ADSI object points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffa89d5b-7ba1-433b-a93d-032012906258">GetCleanupTask</a>
</td>
<td align="left" width="63%">
Returns an interface to the cleanup task associated with the virtual directory. The cleanup task removes orphaned files from the virtual directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edca833f-16ec-40c7-a3d8-f893a635b8e2">GetCleanupTaskName</a>
</td>
<td align="left" width="63%">
Returns the cleanup task name associated with the virtual directory.

</td>
</tr>
</table> 


## -remarks



This interface is registered on the server when you install the BITS server extension.

On Windows Server 2003, use the <b>Windows Components Wizard</b> to install the BITS server extension. From  <b>Control Panel</b>, select <b>Add or Remove Programs</b>. Then, select <b>Add/Remove Windows Components</b> to display the <b>Windows Components Wizard</b>. The BITS server extension is a sub-component of Internet Information Services (IIS) which is a sub-component of Web Application Server.


#### Examples

The following example shows how to use the <b>ADsGetObject</b> function to get a pointer to the 
<b>IBITSExtensionSetup</b> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//Set the BITSUploadEnabled IIS configuration setting.
//The pszPath parameter contains the path to the directory service. 
//For example, "IIS://&lt;machine name&gt;/w3svc/1/&lt;virtual directory&gt;".
//The Enable parameter contains true (enable) or false (disable).
HRESULT SetBITSUploadEnabledSetting(LPWSTR pszPath, bool Enable)
{
  HRESULT hr;
  IBITSExtensionSetup* pExtensionSetup = NULL;

  hr = ADsGetObject(pszPath, __uuidof(IBITSExtensionSetup), &amp;pExtensionSetup);
  if (SUCCEEDED(hr))
  {
    if (Enable)
    {
      hr = pExtensionSetup-&gt;EnableBITSUploads();
    }
    else
    {
      hr = pExtensionSetup-&gt;DisableBITSUploads();
    }

    pExtensionSetup-&gt;Release();
  }

  return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0105d525-c841-4e0e-bd4a-2a1bcdb0dc4a">IBITSExtensionSetupFactory</a>
 

 

