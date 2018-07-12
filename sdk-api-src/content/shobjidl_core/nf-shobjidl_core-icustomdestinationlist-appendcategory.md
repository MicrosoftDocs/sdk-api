---
UID: NF:shobjidl_core.ICustomDestinationList.AppendCategory
title: ICustomDestinationList::AppendCategory
author: windows-sdk-content
description: Defines a custom category and the destinations that it contains, for inclusion in a custom Jump List.
old-location: shell\ICustomDestinationList_AppendCategory.htm
old-project: shell
ms.assetid: 091a2b28-b4cf-46a9-845a-46b5aa86522d
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: AppendCategory, AppendCategory method [Windows Shell], AppendCategory method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],AppendCategory method, ICustomDestinationList.AppendCategory, ICustomDestinationList::AppendCategory, _shell_ICustomDestinationList_AppendCategory, shell.ICustomDestinationList_AppendCategory, shobjidl_core/ICustomDestinationList::AppendCategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICustomDestinationList.AppendCategory
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ICustomDestinationList::AppendCategory


## -description


Defines a custom category and the destinations that it contains, for inclusion in a custom Jump List.


## -parameters




### -param pszCategory [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the display name of the custom category. This string is shown in the category's header in the Jump List. The string can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the category header to be displayed in the user's selected language.

                    

<div class="alert"><b>Note</b>  Each custom category must have a unique name. Duplicate category names will cause presentation issues in the Jump List.</div>
<div> </div>

### -param poa [in]

Type: <b><a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> that represents one or more <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> objects that represent the destinations in the category. Some destinations in the list might also be represented by <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> objects, although less often.

                    

<div class="alert"><b>Note</b>  Any <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> used here must declare an argument list through <a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">SetArguments</a>. Adding an <b>IShellLink</b> object with no arguments to a custom category is not supported since a user cannot pin or unpin this type of item from a Jump List, nor can they be added or removed.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.



If the call to <b>AppendCategory</b> attempts to add an item that is in the removed destinations list retrieved by the call to <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">BeginList</a> that initiated the session, the call to <b>AppendCategory</b> fails.

If <b>AppendCategory</b> attempts to add an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that the application is not registered to handle, the call fails.

<b>AppendCategory</b> can fail if there is a privacy Group Policy or user privacy setting turned on. Custom categories contain user-specific items based on individual usage, which is not allowed under those privacy settings.

A privacy Group Policy or user privacy setting will not cause a failure in any other <a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a> method. Tasks are not user-specific. <a href="https://msdn.microsoft.com/ce73fff3-8d1a-4912-98ce-7149460ffa49">AppendKnownCategory</a> will not result in the display of the <b>Recent</b> or <b>Frequent</b> categories because they will have no data, but the method call will not return a failure code.

In the case of a failure code in <b>AppendCategory</b> caused by privacy Group Policy or user privacy setting (E_ACCESSDENIED), the application should continue to update tasks and call <a href="https://msdn.microsoft.com/5f9aa598-9a94-4210-84cd-f4b39e47b260">CommitList</a>.

If no file type registration was found for the associated application, <b>AppendCategory</b> returns HRESULT 0x80040F03. This can result from an application not registering the file type it is trying to add to the Jump List or from a problem in the registration, such as not providing the AppUserModelID when the application is using an explicit AppUserModelID.




## -remarks



You must call <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">BeginList</a> before you call this method.

If an application provides a custom category, that application assumes responsibility for populating it. The category contents should still be user-specific and based on the user's history and actions, but by using a custom category an application can determine what it wants to track and what it wants to ignore. For instance, different scenarios could be involved when different application options are chosen. For example, an audio program might elect to include only recently played albums and ignore recently played individual tracks. An application might also simply have a usage-tracking algorithm tailored to its specific use that gives better results than the system's default algorithms.

An application can call <b>AppendCategory</b> more than once in a list-building session to add multiple custom categories. In this case, the categories should be designed so that their contents are mutually exclusive. Each custom category should be built around a specific scenario so that items are not duplicated between them.

Categories in a custom Jump List, including the known <b>Recent</b> or <b>Frequent</b> categories, are shown in the order that they are added, with the most recent items added to the end of the list. If there is insufficient space to show all entries, the last entries in the list disappear off the screen first. Therefore, the most important categories should be added first to ensure their best chance of being always shown. Destinations within the category are shown in the order that they are stored in the <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> object pointed to by <i>poa</i>.

The user might decide to pin one or more of the destinations provided in the custom category to the Jump List. The list of pinned destinations is not available to the application, but duplication is prevented by the UI so no extra action is required of the application. Visually, a pinned item moves to the <b>Pinned</b> section of the Jump List and disappears from its original location.

A successful call to <b>AppendCategory</b> does not guarantee that those items will be displayed. Any number of destinations added over the value pointed to by the <i>pcMinItems</i> parameter in <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a> are not shown. The <b>Pinned</b> category takes priority over all other destination lists. The <b>Pinned</b> list is displayed, then the remaining space is allocated to the other destination lists. It is possible for a user to pin enough destinations to the Jump List to keep any other destinations from displaying. Other factors, such as a reduced screen resolution or an increased font size, can also cause application-provided destinations to be truncated from the list. The application has no way of predicting these situations and is not notified when they occur. The application must just be aware that the possibility exists. Because truncation of the destination list or lists occurs from the bottom up, the application should put its most important categories and destinations at the top of the list so that they have the best chance of being shown.

During a session started with <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">BeginList</a> and ending with <a href="https://msdn.microsoft.com/5f9aa598-9a94-4210-84cd-f4b39e47b260">CommitList</a>, you might call <b>AppendCategory</b> more than once. If any one of those calls fails because of an attempt to add a category that contains an item in the removed items list, the call to <b>CommitList</b> does not clear the removed items list. For the removed items list to be cleared, all calls to <b>AppendCategory</b> in a session must return successfully.


<a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> instances provided through the <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> pointed to by <i>poa</i> must provide the following:

                

<ul>
<li>Either a pointer to an item identifier list (PIDL) (<a href="https://msdn.microsoft.com/4c0571a5-1615-4c3f-b9a6-0667df07165b">SetIDList</a>) or the target path (<a href="https://msdn.microsoft.com/032610ba-d6ff-4200-8fd3-455460587dec">SetPath</a> or <a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">SetArguments</a>)</li>
<li>Icon location  (<a href="https://msdn.microsoft.com/1ba267f2-ae05-4a6d-be3c-382a89e17d92">SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="https://msdn.microsoft.com/8fb948d6-2677-4e5d-b283-8757c3df574d">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="https://msdn.microsoft.com/4bec482e-04e6-4cde-ab8e-23c5a1463bdf">SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.




## -see-also




<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/7b254276-dc6f-4d20-8f44-fce8e01b237f">ICustomDestinationList::AddUserTasks</a>



<a href="https://msdn.microsoft.com/ce73fff3-8d1a-4912-98ce-7149460ffa49">ICustomDestinationList::AppendKnownCategory</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

