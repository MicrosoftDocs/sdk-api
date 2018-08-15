---
UID: NN:spellcheck.IUserDictionariesRegistrar
title: IUserDictionariesRegistrar
author: windows-sdk-content
description: Manages the registration of user dictionaries.
old-location: intl\iuserdictionariesregistrar.htm
old-project: Intl
ms.assetid: eca9446a-268e-4318-a5e7-8bb8592c9660
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IUserDictionariesRegistrar, IUserDictionariesRegistrar interface [Internationalization for Windows Applications], IUserDictionariesRegistrar interface [Internationalization for Windows Applications],described, intl.iuserdictionariesregistrar, spellcheck/IUserDictionariesRegistrar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spellcheck.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WORDLIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheck.h
api_name:
 - IUserDictionariesRegistrar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IUserDictionariesRegistrar interface


## -description


Manages the registration of user dictionaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserDictionariesRegistrar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserDictionariesRegistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserDictionariesRegistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dd64e20-af2d-4d84-9e66-01ac19f34212">RegisterUserDictionary</a>
</td>
<td align="left" width="63%">
Registers a file to be used as a user dictionary for the current user, until unregistered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b1756f5-7ab5-4408-896d-5ea5ae671651">UnregisterUserDictionary</a>
</td>
<td align="left" width="63%">
Unregisters a previously registered user dictionary.

</td>
</tr>
</table> 


## -remarks



<b>IUserDictionariesRegistrar</b> allows clients to persistently register and unregister user dictionary files that exist in locations other than the usual dictionary path (<code>%AppData%\Microsoft\Spelling</code>). The dictionaries must have the same file formats as the ones located in the normal path and also should have the appropriate file extensions.
However, it is strongly recommended for clients to place their dictionaries under <code>%AppData%\Microsoft\Spelling</code> whenever possible—the spell checking functionality does not pick up changes in dictionaries outside that directory tree.

This interface is obtained through a <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> in <a href="https://msdn.microsoft.com/7febbb7e-c557-4698-bf58-6e6e7f61b071">ISpellCheckerFactory</a>.

The combined size of all registered dictionary files must be less than 1 MB by default. This can be increased to 2 MB by setting the registry key HKEY_CURRENT_USER\Software\Microsoft\Spelling\Dictionaries\AllowBiggerUD to the value 1. For more information about the Windows registry, see <a href="https://msdn.microsoft.com/library/windows/desktop/ms724871.aspx">Registry</a>.



